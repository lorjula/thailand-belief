<template>
  <div style="background-color:#F7F6F4;">

    <div style="background-color: #ffffff;">

      <Navbar/>

      <div class="">
        <div class="row">
          <div class="col-sm">
            <img class="imgColor" src="~assets/img/belief/carcolor/cover.jpg">
          </div>
        </div>
      </div>
    </div>

    <div class="" style="background-color:#F7F6F4; margin-bottom: 9rem;">
      <div class="container" style="text-align: center;">
        <div class="" style="padding-top: 6rem;">
          <h2 style="color: #A0826A;">สีรถประจําวันเกิด เลือกสีให้เหมาะกับตัวเรา</h2>
          <h5 class="pt-3" style="color: #797979;">
            ก่อนที่จะไปซื้อรถ เราควรรู้นิดหนึ่งกับการเลือกสีรถให้ถูกโฉลกกับวันเกิด หรือสีรถประจำวันเกิด
            การเลืกสีรถไม่ไช้เป็นควมเชื่ออย่างเดียวเเต่ยังช่วยในเรื่องของความสบายใจ
            แต่จะดีไหมถ้าเรารู้ว่าสีไหนถูกกับวันเกิด ใช้แล้วเฮง ใช้แล้วรวยปังๆ หรือสีไหนห้ามใช้ ไปดูกันเลยจ้า
          </h5>
        </div>

        <template v-for="item in birthdayColor">
          <div class="" style="margin-top: 9rem;">
            <div class="row">
              <div class="col-md-4"></div>
              <div class="col-md-4"><img class="imgDay" :src="item.image"></div>
              <div class="col-md-4"></div>

            </div>
            <div class="row" style="margin-top: 5rem;">
              <div class="col-md-1"></div>
              <div class="col-md-10">
                <div class="">
                  <div class="details">
                    <h5 class="topicDay">
                      <table>
                        <tr>
                          <td><b>{{ item.dayTh }}</b></td>
                          <td style="padding-left: 1rem;">"{{ item.dayEn }}"</td>
                        </tr>
                      </table>
                    </h5>
                    <h6 class="codeColor" style="padding-top: 2rem;color: #797979;line-height: 1.6;">
                      <table>
                        <template v-for="m in item.meaning">
                          <tr>
                            <td class="colorCode">{{ m.color }}</td>
                            <td> {{ m.detail }}</td>
                          </tr>
                        </template>
                      </table>
                    </h6>
                  </div>
                </div>
              </div>
              <div class="col-md-1"></div>
            </div>

          </div>
        </template>
      </div>
    </div>
    <Recommended/>

    <Footer/>
  </div>
</template>

<script>
import Navbar from "~/components/nav/navbar";
import Footer from "~/components/footer/footer";
import Recommended from "~/components/belief/recommended";

export default {
  name: "carcolor",
  components: {Recommended, Footer, Navbar},
  data() {
    return {
      birthdayColor: [
        {
          image: require("~/assets/img/belief/carcolor/sunday.png"),
          dayTh: "วันอาทิตย์",
          dayEn: "sunday",
          meaning: [
            {color: "แดง,แดงเลือดหมู", detail: "เสริมสง่าราศี มากด้วยบุญญาบารมี มีอำนาจวาสนา คนนบนอบยำเกรง"},
            {color: "ดำ", detail: "เสริมความน่าเคารพนับถือ เสริมดวงเรื่องทรัพย์สินเงินทอง การเงิน"},
            {color: "ขาว,ครีม", detail: "เสริมความสงบปลอดภัยจากเหตุร้าย เช่น อุบัติเหตุ แคล้วคลาดจากอันตรายทั้งปวง"},
            {
              color: "ม่วงเปลือกมังคุด",
              detail: "เสริมดวงด้านศรัทธา ความน่าเชื่อถือ ความไว้วางใจ และดวงเรื่องการเงิน"
            },
            {color: "เขียว", detail: "เสริมดวงให้คนรักเมตตา อุปถัมภ์ค้ำชู ช่วยเหลือทำให้สะดวกราบรื่นในเรื่องต่าง ๆ"},
            {color: "บรอนซ์,เทา,ทอง", detail: "เสริมดวงเรื่องเมตตามหานิยม เสริมเสน่ห์ การสนับสนุนเกื้อกูล"},
            {color: "ฟ้า,น้ำเงิน", detail: "เป็นกาลกิณีไม่นิยมใช้"},
          ]
        },
        {
          image: require("assets/img/belief/carcolor/c2.png"),
          dayTh: "วันจันทร์",
          dayEn: "Monday",
          meaning: [
            {
              color: "ส้ม,เหลืองแก่",
              detail: "เสริมดวงเรื่องการเงิน ความมั่นคง ทุนทรัพย์ ราคาและคุณค่าที่จะเพิ่มพูนให้แก่ตนเองในปัจจุบันและภายภาคหน้า"
            },
            {color: "ดำ", detail: "เสริมความสงบปลอดภัยจากเหตุร้าย เช่น อุบัติเหตุ แคล้วคลาดจากอันตรายทั้งปวง"},
            {
              color: "น้ำเงิน,ทอง",
              detail: "เสริมเสน่ห์ ผู้ใหญ่รักเมตตาและเอ็นดู มีแต่สิ่งที่เป็นสิริมงคลแก่ชีวิต หลักทรัพย์ โชคลาภ เสน่ห์ที่ทำให้คนรักใคร่เมตตา และศรัทธาในตัวเรา"
            },
            {color: "ม่วงเปลือกมังคุด", detail: "เสริมดวงด้านความสะดวกราบรื่นทุกอย่าง"},
            {
              color: "ชมพู",
              detail: "เสริมดวงให้ประสบผลสำเร็จได้รับการอุปถัมภ์ค้ำชู ได้รับการสงเคราะห์เกื้อหนุนจากผู้ใหญ่ ได้รับการส่งเสริม ในการดำเนินชีวิตและหน้าที่การงาน"
            },
            {color: "ฟ้า", detail: "เสริมดวงให้ประสบความสำเร็จในการดำเนินชีวิตและหน้าที่การงาน"},
            {
              color: "เขียว",
              detail: "อำนาจวาสนา บารมี เกียรติยศ และชื่อเสียงตำแหน่งหน้าที่การงาน อานุภาพอิทธิพลที่ทำให้คนเคารพยำเกรง มีความสามารถในการควบคุมบังคับบัญชาคน"
            },
            {color: "แดง", detail: "เป็นกาลกิณีไม่นิยมใช้"},
          ]
        },
        {
          image: require("assets/img/belief/carcolor/c3.png"),
          dayTh: "วันอังคาร",
          dayEn: "Tuesday",
          meaning: [
            {color: "ม่วงแก่", detail: "เสริมวาสนาบารมี โชคลาภ ความโชคดี"},
            {
              color: "ดำ",
              detail: "เสริมดวงด้านพลังอำนาจ เกียรติยศ และชื่อเสียงตำแหน่งหน้าที่การงาน อานุภาพอิทธิพลที่ทำให้คนเคารพยำเกรง มีความสามารถในการควบคุมบังคับ"
            },
            {color: "บรอนซ์,เทา", detail: "เสริมความน่าเชื่อถือ ความไว้วางใจ"},
            {color: "ทอง,แสด", detail: "เสริมความสงบปลอดภัยจากเหตุร้าย เช่น อุบัติเหตุ แคล้วคลาดจากอันตรายทั้งปวง"},
            {
              color: "น้ำตาล",
              detail: "เสริมดวงด้านความมั่นคงในชีวิต เช่น มั่นคงเรื่องหลักทรัพย์ ทรัพย์สิน หน้าที่การงาน"
            },
            {color: "เขียว", detail: "เสริมดวงด้านการแก้ปัญหา ไร้อุปสรรค ไร้ศัตรูและคู่แข่ง"},
            {
              color: "แดง,ชมพู",
              detail: "เสริมดวงให้ประสบผลสำเร็จ ได้รับการอุปถัมภ์ค้ำชู ได้รับการสงเคราะห์เกื้อหนุนจากผู้ใหญ่ ได้รับการส่งเสริมในการดำเนินชีวิตและหน้าที่การงาน"
            },
            {color: "ขาว,เหลือง", detail: "เป็นกาลกิณีไม่นิยมใช้"},
          ]
        },
        {
          image: require("assets/img/belief/carcolor/c4.png"),
          dayTh: "วันพุธกลางวัน",
          dayEn: "Wednesday Lunch",
          meaning: [
            {color: "น้ำเงิน,ฟ้า", detail: "เสริมดวงด้านความเคารพนับถือ ยกย่อง ยอมรับ"},
            {
              color: "น้ำตาล,ทอง",
              detail: "เสริมดวงด้านพลังอำนาจ เกียรติยศ และชื่อเสียง ตำแหน่งหน้าที่การงาน อานุภาพอิทธิพลที่ทำให้คนเคารพยำเกรง มีความสามารถในการควบคุมบังคับ"
            },
            {
              color: "ขาว,เหลืองอ่อน",
              detail: "เสริมดวงให้ประสบผลสำเร็จได้รับการอุปถัมภ์ค้ำชู ได้รับการสงเคราะห์เกื้อหนุนจากผู้ใหญ่ ได้รับการส่งเสริมในการดำเนินชีวิตและหน้าที่การงาน"
            },
            {
              color: "เทา,บรอนซ์",
              detail: "เสริมความสงบปลอดภัยจากเหตุร้าย เช่น อุบัติเหตุ แคล้วคลาดจากอันตรายทั้งปวง"
            },
            {
              color: "ดำ",
              detail: "เสริมดวงด้านการแก้ปัญหา ไร้อุปสรรค ไร้ศัตรูและคู่แข่ง ชีวิตมีแต่ความสะดวก ราบรื่น"
            },
            {color: "ม่วงแก่", detail: "เสริมโชควาสนา เสริมวาสนาบารมี โชคลาภ ความโชคดี"},
            {color: "เขียว", detail: "เสริมดวงด้านเสน่ห์ที่ทำให้คนรักใคร่เมตตา และศรัทธาในตัวเรา"},
            {color: "ชมพู", detail: "เป็นกาลกิณีไม่นิยมใช้"},
          ]
        },
        {
          image: require("assets/img/belief/carcolor/c5.png"),
          dayTh: "วันพุธกลางคืน",
          dayEn: "Wednesday Night",
          meaning: [
            {color: "ชมพู", detail: "เสริมดวงให้คนเชื่อถือและไว้วางใจ"},
            {color: "ดำ", detail: "เสริมดวงด้านความเจริญรุ่งเรืองในหน้าที่การงาน"},
            {
              color: "เทา,บรอนซ์",
              detail: "เสริมความสงบปลอดภัยจากเหตุร้าย เช่น อุบัติเหตุ แคล้วคลาดจากอันตรายทั้งปวง"
            },
            {
              color: "ม่วงแก่",
              detail: "เสริมดวงให้ประสบผลสำเร็จ ได้รับการอุปถัมภ์ค้ำชู ได้รับการสงเคราะห์เกื้อหนุนจากผู้ใหญ่ ได้รับการส่งเสริม ในการดำเนินชีวิตและหน้าที่การงาน"
            },
            {
              color: "น้ำเงิน,ฟ้า",
              detail: "เสริมดวงด้านการแก้ปัญหา ไร้อุปสรรค ไร้ศัตรูและคู่แข่ง ชีวิตมีแต่ความสะดวก ราบรื่น"
            },
            {color: "แดง,น้ำตาล", detail: "เสริมโชควาสนา เสริมวาสนาบารมี โชคลาภ ความโชคดี"},
            {color: "ม่วง,ดำ", detail: "เสริมสร้างเมตาของคนอุปถัมถ์ค้ำชู ช่วยเหลือ"},
            {color: "ส้ม,ทอง", detail: "เป็นกาลกิณีไม่นิยมใช้"},
          ]
        },
        {
          image: require("assets/img/belief/carcolor/c6.png"),
          dayTh: "วันพฤหัสบดี",
          dayEn: "Thursday",
          meaning: [
            {color: "ขาว", detail: "เสริมดวงให้คนเชื่อถือและไว้วางใจ"},
            {color: "แดง", detail: "เสริมดวงด้านความสงบปลอดภัยจากเหตุร้าย เช่น อุบัติเหตุ แคล้วคลาดจากอันตรายทั้งปวง"},
            {
              color: "เทา,บรอนซ์",
              detail: "เสริมดวงด้านการแก้ปัญหา ไร้อุปสรรค ไร้ศัตรูและคู่แข่ง ชีวิตมีแต่ความสะดวก ราบรื่น"
            },
            {color: "ฟ้า", detail: "เสริมโชควาสนา เสริมวาสนาบารมี โชคลาภ ความโชคดี"},
            {
              color: "เขียว",
              detail: "เสริมดวงให้ประสบผลสำเร็จได้รับการอุปถัมภ์ค้ำชู ได้รับการสงเคราะห์เกื้อหนุนจากผู้ใหญ่ ได้รับการส่งเสริม ในการดำเนินชีวิตและหน้าที่การงาน"
            },
            {
              color: "ส้ม,ทอง",
              detail: "เสริมความเป็นสิริมงคลแก่ชีวิต หลักทรัพย์ โชคลาภ เสน่ห์ที่ทำให้คนรักใคร่เมตตา และศรัทธาในตัวเรา"
            },
            {color: "ดำ,ม่วง,น้ำเงิน ", detail: "เป็นกาลกิณีไม่นิยมใช้"},
          ]
        },
        {
          image: require("assets/img/belief/carcolor/c7.png"),
          dayTh: "วันศุกร์",
          dayEn: "Friday",
          meaning: [
            {color: "เขียว", detail: "เสริมดวงให้คนเชื่อถือและไว้วางใจ"},
            {color: "แดง,ทอง", detail: "เสริมดวงด้านความก้าวหน้าเจริญรุ่งเรืองในหน้าที่การงาน"},
            {
              color: "แดง,ชมพู",
              detail: "เสริมดวงด้านความสงบปลอดภัยจากเหตุร้าย เช่น อุบัติเหตุ แคล้วคลาดจากอันตรายทั้งปวง"
            },
            {
              color: "เหลือง",
              detail: "เสริมดวงให้ประสบผลสำเร็จ ได้รับการอุปถัมภ์ค้ำชู ได้รับการสงเคราะห์เกื้อหนุนจากผู้ใหญ่ ได้รับการส่งเสริม ในการดำเนินชีวิตและหน้าที่การงาน"
            },
            {color: "ดำ", detail: "เสริมดวงด้านการแก้ปัญหา ไร้อุปสรรค ไร้ศัตรูและคู่แข่ง ชีวิตมีแต่ความสะดวก ราบรื่น"},
            {color: "น้ำตาล", detail: "เสริมโชควาสนา เสริมวาสนาบารมี โชคลาภ ความโชคดี"},
            {
              color: "ฟ้า,น้ำเงิน",
              detail: "เสริมความเป็นสิริมงคลแก่ชีวิต หลักทรัพย์ โชคลาภ เสน่ห์ที่ทำให้คนรักใคร่เมตตา และศรัทธาในตัวเรา"
            },
            {color: "เทา,บรอนซ์,ม่วง", detail: "เป็นกาลกิณีไม่นิยมใช้"},

          ]
        },
        {
          image: require("assets/img/belief/carcolor/c8.png"),
          dayTh: "วันเสาร์",
          dayEn: "Saturday",
          meaning: [
            {color: "แดง", detail: "เสริมดวงให้คนยอมรับเชื่อถือและไว้วางใจ"},
            {
              color: "ชมพู",
              detail: "เสริมดวงให้ประสบผลสำเร็จ ได้รับการอุปถัมภ์ค้ำชู ได้รับการสงเคราะห์เกื้อหนุนจากผู้ใหญ่ ได้รับการส่งเสริม ในการดำเนินชีวิตและหน้าที่การงาน"
            },
            {
              color: "น้ำเงิน,ฟ้า",
              detail: "เสริมดวงด้านความสงบปลอดภัยจากเหตุร้าย เช่น อุบัติเหตุ แคล้วคลาดจากอันตรายทั้งปวง"
            },
            {color: "เทา,บรอนซ์", detail: "เสริมโชควาสนา เสริมวาสนาบารมี โชคลาภ ความโชคดี"},
            {
              color: "ทอง,เหลือง",
              detail: "เสริมดวงด้านการแก้ปัญหา ไร้อุปสรรค ไร้ศัตรูและคู่แข่ง ชีวิตมีแต่ความสะดวก ราบรื่น"
            },
            {
              color: "ดำ,ม่วงแก่",
              detail: "เสริมความเป็นสิริมงคลแก่ชีวิต หลักทรัพย์ โชคลาภ เสน่ห์ที่ทำให้คนรักใคร่เมตตา และศรัทธาในตัวเรา"
            },
            {color: "เขียว,แสด", detail: "เป็นกาลกิณีไม่นิยมใช้"},
          ]
        },
      ]
    }
  }
}
</script>

<style scoped>

.col-sm {
  padding: 0;
}

.imgColor {
  object-fit: cover;
  width: 100%;
  height: 20rem;
}

.imgDay {
  width: 100%;
}

.topicDay {
  padding-top: 0px;
  color: #737d75;
}


.codeColor {
  font-size: 1.1rem;
}

.colorCode {
  padding-right: 2rem;
  color: #be977a;
}


/*iphone5/se*/
@media only screen and (max-width: 320px) {
  .pt-3 {
    margin-left: 2rem;
    margin-right: 2rem;
    line-height: 1.6;
  }

  .details {
    text-align: left;
    padding-top: 0px;
    padding-right: 1rem;
    padding-left: 1rem;

  }
}

/*Galaxys5*/
@media only screen and (min-width: 360px) {
  .pt-3 {
    margin-left: 2rem;
    margin-right: 2rem;
  }

  .details {
    text-align: left;
    padding-top: 0px;
    padding-right: 1rem;
    padding-left: 1rem;

  }
}

/*iphone 6/7/8*/
@media only screen and (min-width: 375px) {
  .pt-3 {
    margin-left: 2rem;
    margin-right: 2rem;
  }

  .details {
    text-align: left;
    padding-top: 0px;
    padding-right: 1rem;
    padding-left: 1rem;

  }
}

/*I678plus*/
@media only screen and (min-width: 414px) {
  .pt-3 {
    margin-left: 2rem;
    margin-right: 2rem;
  }

  .details {
    text-align: left;
    padding-top: 0px;
    padding-right: 1rem;
    padding-left: 1rem;

  }
}

/*surfaceDuo*/
@media only screen and (min-width: 540px) {
  .pt-3 {
    margin-left: 2rem;
    margin-right: 2rem;
  }

  .details {
    text-align: left;
    padding-top: 0px;
    padding-right: 1rem;
    padding-left: 1rem;

  }
}

/*ipad*/
@media only screen and (min-width: 768px) {
  .pt-3 {
    margin-left: 4rem;
    margin-right: 4rem;
  }

  .details {
    text-align: left;
    padding-top: 0px;
    padding-right: 3rem;
    padding-left: 3rem;

  }
}

/*ipadPro*/
@media only screen and (min-width: 1024px) {
  pt-3 {
    margin-left: 4rem;
    margin-right: 4rem;
  }

  .details {
    text-align: left;
    padding-top: 0px;
    padding-right: 3rem;
    padding-left: 3rem;

  }
}

/*pc*/
@media only screen and (min-width: 1024px) {
  .pt-3 {
    margin-left: 9rem;
    margin-right: 9rem;
    line-height: 1.6;
  }

  .details {
    text-align: left;
    padding-top: 0px;
    padding-right: 3rem;
    padding-left: 3rem;

  }

}
</style>
