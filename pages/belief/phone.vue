<template>
  <div style="background-color:#F7F6F4;">

    <div style="background-color: #f7f6f4;">

      <Navbar/>

      <div class="container">
        <div class="row">
          <div class="col-sm">
            <img class="imgColor" src="~assets/img/belief/phone/cover.jpeg" style="border-radius: 4px;">
          </div>
        </div>
      </div>
    </div>

    <div class="" style="background-color:#F7F6F4; margin-bottom: 9rem;">
      <div class="container" style="text-align: center;">
        <div class="" style="padding-top: 6rem;">
          <h2 style="color: #A0826A;">เคล็ดลับ!..เลือกสีเคสมือถือให้รุ่ง ให้ปังปังจ้า</h2>
          <h5 class="pt-3" style="color: #797979;">
            ในยุคปัจจุบันนี้มีศาสตร์มากมาย ความเชื่อหลากหลายรูปแบบไม่ว่าจะเป็นสีกระเป๋าตัง สีรถที่เป็นมงคล
            การจัดบ้านเลือกสีท่าบ้านให้ถูกโฉลกกับคนที่อยู่อาศัย และอีกสิ่งหนึ่งที่ยังมาแรงเช่นกันก็คือ
            การเลือกเคศมือถือไม่ไช่เเค่เรื่องความสวยงามหรือความชอบอย่างเดียวน่ะค่ะแต่จะมีความเชื่อในเรื่องของการเลือกสีเคสในถูกโฉลกกับตัวเรา
            ด้วยความเชื่อนั้น มีความเชื่อว่าถ้าเลือกสีเคสให้ถูกกับวันเกิดของเรานั้นจะช่วยในเรื่องของความเสริมสิริมงคล
            เสริมเรื่องการเงิน, การงาน, เรื่องความรัก วันนี้เราก็มีเราก็มีการเลือกสีเคศให้เหมาะกับวันเกิดของเพื่อนๆ
            ไปดูกันเลยค่ะ
          </h5>
        </div>

        <template v-for="item in birthdayColor">
          <div class="" style="margin-top: 9rem;">
            <div class="row">
              <div class="col-md-6">
                <img class="imgDay" :src="item.image">
              </div>

              <div class="col-md-6 coldetails">
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
                <div class="col-md-1"></div>
              </div>

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
import Footer from "~/components/footer/footer";
import Navbar from "~/components/nav/navbar";
import Recommended from "~/components/belief/recommended";

export default {
  name: "phone",
  components: {Recommended, Navbar, Footer},
  data() {
    return {
      birthdayColor: [
        {
          image: require("~/assets/img/belief/phone/p1.png"),
          dayTh: "วันอาทิตย์",
          dayEn: "sunday",
          meaning: [
            {
              detail: "ก็คือ สีดำ สีเทา สีน้ำตาล เสริมเสน่ห์ ความมั่นใจในตัวเอง การเจรจา การเงินการงานเจริญรุ่งเรืองทั้งนี้ทั้งนั้นเรื่องเหล่านี้ก็เป็นความเชื่อแต่ละบุคคล ใครไม่เชื่อก็ไม่เป็นอะไรน๊า แค่เป็นคนดี คิดดี ทำดี ก็จะมีแต่สิ่งดีๆเข้ามาแล้วจร้า"
            },
          ]
        },
        {
          image: require("assets/img/belief/phone/p2.png"),
          dayTh: "วันจันทร์",
          dayEn: "Monday",
          meaning: [
            {detail: "ก็คือ สีเขียว สีน้ำเงิน ซึ่งจะมาเสริมในเรื่องของการเงิน จะมีเงินเข้ามาเรื่อยๆไม่ขาดมือ เรื่องความเจริญรุ่งเรืองในหน้าที่การงาน รวมถึงโอกาสดีๆที่จะเข้ามาด้วย มีแต่คนให้ความช่วยเหลือ ผู้ใหญ่รักเอ็นดูเมตตา พร้อมทั้งยังเสริมในเรื่องของอำนาจ วาสนาบารมีอีกด้วย"},
          ]
        },
        {
          image: require("assets/img/belief/phone/p3.png"),
          dayTh: "วันอังคาร",
          dayEn: "Tuesday",
          meaning: [
            {
              detail: "ก็คือ สีเงิน สีทอง สีเหล่านี้จะช่วยเสริมในเรื่องอำนาจ การเจรจาไม่ว่าจะพูดติดต่อ สื่อสาร หรือสัมภาษณ์งานก็ง่าย ไหลลื่นไปหมด การเงินคล่องตัว มีคนคอยอุปถัมภ์ค้ำชู"
            },
          ]
        },
        {
          image: require("assets/img/belief/phone/p4.png"),
          dayTh: "วันพุธกลางวัน",
          dayEn: "Wednesday Lunch",
          meaning: [
            {detail: "ก็คือ สีเหลือง สีฟ้า สีน้ำเงิน ช่วยเสริมในเรื่องของความรัก มีเสน่ห์ คนอุปถัมภ์ การเงินไหลมาเทามา การงาน อำนาจ เพื่อนๆคนไหนที่ยังโสดอยู่รอเปลี่ยนมาใช้สีเหล่านี้ดูนะจ๊ะ"},
          ]
        },
        {
          image: require("assets/img/belief/phone/p5.png"),
          dayTh: "วันพุธกลางคืน",
          dayEn: "Wednesday Night",
          meaning: [
            {detail: " สีดำ สีขาวนวล สีชมพู สีกลุ่มนี้เป็นโทนสีที่ถูกโฉลกกับคนเกิดวันพุธตอนกลางคืน เสริมสร้างเมตตาของคนอุปถัมถ์ค้ำชู ช่วยเหลือ เสริมสร้างเสน่ห์เมตตาให้คนหลงใหล"},
          ]
        },
        {
          image: require("assets/img/belief/phone/p6.png"),
          dayTh: "วันพฤหัสบดี",
          dayEn: "Thursday",
          meaning: [
            {detail: "ก็คือ สีน้ำเงิน สีเทา ช่วยเสริมอำนาจ บารมี ในเรื่องเพื่อนฝูง การงาน การเงิน ความรัก เพื่อนๆคนไหนที่รู้สึกว่าช่วงนี้ทำไมงานไม่ค่อยราบลื่นเลย ทำอะไรก็ติดขัด ลองเปลี่ยนสีเคสดูอาจจะดีขึ้นก็ได้นะ ต้องลองๆ"},

          ]
        },
        {
          image: require("assets/img/belief/phone/p7.png"),
          dayTh: "วันศุกร์",
          dayEn: "Friday",
          meaning: [
            {detail: "ก็คือ สีส้ม สีแดง สีทอง ช่วยเสริมในเรื่องของความก้าวหน้า มั่นคง ประสบความสำเร็จ การเงิน การงาน ที่สำคัญช่วยในเรื่องโชคลาภด้วย"},

          ]
        },
        {
          image: require("assets/img/belief/phone/p8.png"),
          dayTh: "วันเสาร์",
          dayEn: "Saturday",
          meaning: [
            {detail: "ก็คือ สีม่วง สีชมพู สีดำ เสริมในเรื่องการพูดจาพูดแล้วมีแต่คนคล้อยตาม การเงิน การงาน ทำงานไหลลื่นไม่มีปัญหาติดขัด โชคลาภ"},
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
  padding: 3rem;
}

.topicDay {
  padding-top: 3rem;
  color: #737d75;
}

.details {
  text-align: left;
  padding: 3rem;

}

.codeColor {
  font-size: 1.1rem;
}

.colorCode {
  color: #be977a;
}


/*iphone5/se*/
@media only screen and (max-width: 320px) {
  .pt-3 {
    margin-left: 1rem;
    margin-right: 1rem;
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
    margin-left: 1rem;
    margin-right: 1rem;
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
    margin-left: 1rem;
    margin-right: 1rem;
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
    margin-left: 1rem;
    margin-right: 1rem;
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

  .coldetails {
    margin-top: 5rem;
  }

}
</style>
