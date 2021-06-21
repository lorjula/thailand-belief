<template>
  <div style="background-color:#F7F6F4;">

    <div style="background-color: #f7f6f4;;">

      <Navbar/>

      <div class="row">
        <div class="col-sm">
          <img class="imgColor" src="~assets/img/belief/bed-sheet/cover.jpg">
        </div>
      </div>

    </div>

    <div class="" style="background-color:#F7F6F4; margin-bottom: 9rem;">
      <div class="container" style="text-align: center;">
        <div class="" style="padding-top: 6rem;">
          <h2 style="color: #A0826A;">สีผ้าปูที่นอนถูกโฉลกตามวันเกิด</h2>
          <h5 class="pt-3" style="color: #797979;">
            การเลือกสีที่นอนให้ถูกโฉลก เป็นส่วนสำคัญที่ช่วยเสริมดวงให้ดีมากยิ่งขึ้น ไม่ว่าจะเป็นด้านสุขภาพ การงาน
            การเงิน รวมไปถึงด้านความรัก การเลือกใช้สีผ้าปูที่นอนให้เหมาะกับวันเกิด
            ให้สุดปังมาฝากกัน เกิดวันไหนมาดูเลยว่าควรเลือกผ้าปูที่นอนสีอะไรดี เสริมดวงให้ปัง ๆ
          </h5>
        </div>

        <template v-for="item in birthdayColor">
          <div class="" style="margin-top: 9rem;">
            <div class="row">
              <div class="col-md-4"></div>
              <div class="col-md-4">
                <img class="imgDay" :src="item.image">

                <a :href="item.link.to" style="text-decoration:none;">
                  <h6 class="link">{{ item.link.display }}</h6>
                </a>

              </div>

              <div class="col-md-4"></div>

            </div>
            <div class="row" style="margin-top: 5rem;">
              <div class="col-md-2"></div>
              <div class="col-md-8">
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
                      <div style="padding-top: 2rem;color: #797979;">
                        <table>
                          <template v-for="m in item.meaning">
                            <tr>{{ m.auspicious }}</tr>
                          </template>
                        </table>
                      </div>
                      <div style="padding-top: 1rem;color: #ad434b;">
                        <table>
                          <template v-for="m in item.meaning">
                            <tr>{{ m.limitation }}</tr>
                          </template>
                        </table>
                      </div>
                    </h6>
                  </div>
                </div>
              </div>
              <div class="col-md-2"></div>
            </div>

          </div>
        </template>
        <a class="dataSource" href="https://nocnoc.com/blog/how-to-choose-bed-sheet-color-by-your-date-of-birth/"
           style="text-decoration:none;">
          <h5>ที่มา:https://nocnoc.com</h5>
        </a>

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
  name: "bed",
  components: {Recommended, Footer, Navbar},
  data() {
    return {
      birthdayColor: [
        {
          image: require("~/assets/img/belief/bed-sheet/b1.png"),
          link: {
            to: "https://www.pinterest.com/pin/336433034668438086/",
            display: "www.pinterest.com",
          },
          dayTh: "วันอาทิตย์",
          dayEn: "sunday",
          meaning: [
            {
              color: "เขียว",
              detail: "ส่งเสริมความโรแมนติกในเรื่องความรัก สำหรับคนโสดการเลือกสีผ้าปูที่นอนด้วยเฉดสีเหล่านี้ก็จะช่วยเพิ่มพลังดึงดูดความรักได้"
            },
            {color: "ฟ้า,น้ำเงิน", detail: "สีกาลกิณี"},
            {auspicious: "คนเกิดวันอาทิตย์ มักเป็นคนที่มีความเป็นผู้นำ ทะเยอทะยาน ค่อนข้างใจร้อนจนบางครั้งเหมือนกับคนดื้อเลยทีเดียว สำหรับผ้าปูที่นอนถูกโฉลกคนวันอาทิตย์ได้แก่ สีเขียวทั้งเขียวแก่ หรือเขียวอ่อน และสีโทนอ่อน เช่น สีขาวหรือสีเหลือง ควรหลีกเลี่ยงผ้าปูที่นอนสีฟ้าหรือสีน้ำเงิน"},
          ]
        },
        {
          image: require("assets/img/belief/bed-sheet/b2.png"),
          link: {
            to: "https://www.pinterest.com/pin/447967494193096674/",
            display: "www.pinterest.com",
          },
          dayTh: "วันจันทร์",
          dayEn: "Monday",
          meaning: [
            {color: "ม่วงอ่อน,ม่วงเข้ม", detail: "ส่งเสริมเรื่ิองดึงดูดความมั่นใจให้กับคนเกิดวันอังคารได้"},
            {color: "แดง", detail: "สีกาลกิณี"},
            {auspicious: "คนที่เกิดวันจันทร์มักเป็นคนอัธยาศัยดี ใจดีต่อผู้อื่น แต่ก็เป็นคนที่ตัดสินใจอะไรไม่ค่อยได้มักโลเลได้ง่าย ควรเลือกใช้สีเขียวและสีม่วงไม่ว่าจะเป็นม่วงอ่อนหรือม่วงเข้ม ควรหลีกเลี่ยงการใช้ผ้าปูที่นอนสีแดง"},
          ]
        },
        {
          image: require("assets/img/belief/bed-sheet/b3.png"),
          link: {
            to: "https://nocnoc.com/blog/how-to-choose-bed-sheet-color-by-your-date-of-birth/",
            display: "https://nocnoc.com",
          },
          dayTh: "วันอังคาร",
          dayEn: "Tuesday",
          meaning: [
            {color: "แดง", detail: "ช่วยเพิ่มเสน่ห์และช่วยดึงดูดความรักที่ดีให้กับคนที่เกิดวันนี้"},
            {color: "เหลืองอ่อน,ขาว", detail: "สีกาลกิณี"},
            {auspicious: "คนเกิดวันอังคารมักเป็นตรงไปตรงมา จริงจังแต่ก็เป็นคนจิตใจดี ปรับตัวได้กับหลายสถานการณ์และมีความคิดสร้างสรรค์  สีที่นอนถูกโฉลกของคนวันเกิดวันอังคาร สีม่วง สีแดงรวมไปถึงสีแสด แต่ควรหลีกเลี่ยงการใช้สีเหลืองและสีขาว"},
          ]
        },
        {
          image: require("assets/img/belief/bed-sheet/b4.png"),
          link: {
            to: "https://www.pinterest.com/pin/135389532535704001/",
            display: "www.pinterest.com",
          },
          dayTh: "วันพุธ",
          dayEn: "Wednesday",
          meaning: [
            {color: "เขียว", detail: "ส่งเสริมให้มั่นใจมากขึ้นสร้างจิตให้เข้มแข็ง "},
            {color: "ชมพู", detail: "สีกาลกิณี"},
            {auspicious: " คนเกิดวันพุธถือเป็นสื่อสาร เป็นนักพูด ช่างคิดแต่ก็รอบคอบ มีความรับผิดชอบและมีความเป็นผู้นำสูงมาก โดยสีผ้าปูที่นอนตามวันเกิดของคนวันพุธคือสีเขียวได้ทุกเฉด เช่น เขียวอ่อน เขียวแก่ เขียวขี้ม้า สีเหลืองทั้งเหลืองอ่อนและเหลืองเข้ม และควรหลีกเลี่ยงผ้าปูที่นอนสีชมพู "},

          ]
        },
        {
          image: require("assets/img/belief/bed-sheet/b6.png"),
          link: {
            to: "https://www.pinterest.com/pin/803611127261688995/",
            display: "www.pinterest.com",
          },
          dayTh: "วันพฤหัสบดี",
          dayEn: "Thursday",
          meaning: [
            {color: "ฟ้า,น้ำเงิน,เขียว", detail: "ช่วยให้ผ่อนคลายมากยิ่งขึ้น"},
            {color: "ม่วง", detail: "สีกาลกิณี"},
            {auspicious: "ความสงบสันติเป็นนิสัยที่สำคัญของคนเกิดวันพฤหัสบดี แต่ถึงจะเป็นคนรักความสงบแต่คนเกิดวันนี้ก็ยังชอบความสำเร็จและจริงจังกับทุกเรื่องซึ่งทำให้เกิดความเครียดได้ง่ายมาก ดังนั้นสีผ้าปูที่นอนถูกโฉลกจึงหนีไม่พ้นสีโทนอ่อนอย่างสีฟ้า สีน้ำเงิน สีเขียว หรือจะเลือกใช้ผ้าปูที่นอนสีแดงด้วยก็ได้เช่นกัน แต่ควรหลีกเลี่ยงสีม่วงทั้งโทนอ่อนและเข้ม"},
          ]
        },
        {
          image: require("assets/img/belief/bed-sheet/b7.png"),
          link: {
            to: "https://www.pinterest.com/pin/88172105192637829/",
            display: "www.pinterest.com",
          },
          dayTh: "วันศุกร์",
          dayEn: "Friday",
          meaning: [
            {color: "ชมพู", detail: "ส่งเสริมความสัมพันธ์กับคนรอบตัวให้ดียิ่งขึ้น"},
            {color: "เขียวแก่", detail: "สีกาลกิณี"},
            {auspicious: "คนเกิดวันศุกร์เป็นคนรักสวยรักงาม ใส่ใจรายละเอียดในตัวเอง เป็นคนมีระเบียบ ฉลาดและมีความรู้รอบตัวอยู่เยอะ อีกทั้งเป็นที่รักของคนรอบตัว ควรเลือกใช้ผ้าปูที่นอนสีเหลือง สีชมพูอ่อนรวมถึงสีแสดเพื่อช่วยส่งเสริมความสัมพันธ์กับคนรอบตัวให้ดียิ่งขึ้น แต่ควรหลีกเลี่ยงการใช้ผ้าปูที่นอนสีเขียวแก่"},
          ]
        },
        {
          image: require("assets/img/belief/bed-sheet/b8.png"),
          link: {
            to: "https://www.pinterest.com/pin/7670261854281423/",
            display: "www.pinterest.com",
          },
          dayTh: "วันเสาร์",
          dayEn: "Saturday",
          meaning: [
            {
              color: "น้ำเงิน,ฟ้า",
              detail: "ซึ่งช่วยส่งเสริมดวงด้านความรักช่วยส่งเสริมความโรแมนติก ความอ่อนหวานและส่งเสริมเรื่องความรักที่มั่นคง"
            },
            {color: "เขียวแก่", detail: "สีกาลกิณี"},
            {auspicious: "สีที่นอนถูกโฉลกกับคนเกิดวันเสาร์ได้แก่สีน้ำเงิน สีฟ้า สีน้ำตาลและสีชมพู โดยควรหลีกเลี่ยงผ้าปูที่นอนสีเขียวทั้งเขียวสดและเขียวอ่อน"},
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

.link {
  font-size: 0.7rem;
  color: #a4a3a3;
}

.link:hover {
  color: #be977a;
}

.dataSource {
  font-size: 1rem;
  color: #a4a3a3;
}

.dataSource:hover {
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
