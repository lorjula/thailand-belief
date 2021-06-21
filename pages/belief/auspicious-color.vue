<template>
  <div style="background-color:#F7F6F4; ">

    <div style="background-color: #ffffff;">
      <Navbar/>
      <div class="container">
        <div class="row">
          <div class="col-sm">
            <img class="imgColor" src="~assets/img/belief/auspiciouscolor/c1.png">
          </div>
        </div>
      </div>
    </div>

    <div class="" style="background-color:#F7F6F4; margin-bottom: 9rem;">
      <div class="container" style="text-align: center;">
        <div class="" style="padding-top: 6rem;">
          <h2 style="color: #A0826A;">สีมงคล,กาลกิณีประจำวันเกิด</h2>
          <h5 class="pt-3" style="color: #797979;">สีมงคล
            ตามวันเกิด เลือกใช้ให้เป็นมงคลกับตัว เสริมดวง ในด้านต่างๆให้ดีขึ้นซึ่งการเลือกสีเสื้อผ้าหรือสีที่เป็นมงคล
            กับตัวเป็นสิ่งที่ทำกันมาตั้งแต่โบราณกาลทั้งนี้ตามความเชื่อ
            ทางโหราศาสตร์หากเลือกใช้สีที่เป็นมงคลก็จะส่งเสริมตัว ทั้งในเรื่องของโชคลาภ บริวาร เสน่ห์
            แต่ถ้าหากใช้สีที่เป็น กาลกิณีกับตัว ก็จะขัดโชค ขัดลาภ หรืออาจจะมีสิ่งต่างๆ ที่ไม่เป็นมงคลเกิดขึ้นได้</h5>
        </div>

        <template v-for="item in birthdayColor">
          <div class="row rowimg">
            <div class="col-md-6 ">
              <img class="imgDay" :src="item.image">
            </div>
            <div class="col-md-6 ">
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
                        <td style="padding-left: 1rem"> {{ m.detail }}</td>
                      </tr>
                    </template>
                  </table>
                </h6>
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
import Navbar from "~/components/nav/navbar";
import Footer from "~/components/footer/footer";
import Recommended from "~/components/belief/recommended";

export default {
  name: "auspicious-color",
  components: {Recommended, Footer, Navbar},
  data() {
    return {
      birthdayColor: [
        {
          image: require("~/assets/img/belief/auspiciouscolor/sunday.svg"),
          dayTh: "วันอาทิตย์",
          dayEn: "sunday",
          meaning: [
            {color: "สีแดง", detail: "เสริมสร้างบริวาร"},
            {color: "สีขาว,เหลือง", detail: "เสริมสร้างให้มีสุขภาพที่แข็งแรง"},
            {color: "สีชมพู", detail: "เสริมสร้างให้ดูมีสง่าราศี"},
            {color: "สีเขียว", detail: "เสริมสร้างเสน่ห์เมตตาให้คนหลงใหล"},
            {color: "สีม่วง,ดำ", detail: "เสริมด้านโชคลาภให้ทำมาค้าคล่อง"},
            {color: "สีส้ม", detail: "เสริมสร้างจิตให้เข้มแข็ง สร้างความสำเร็จ\n"},
            {color: "สีเทา", detail: "เสริมสร้างเมตาของคนอุปถัมถ์ค้ำชู ช่วยเหลือ"},
            {color: "สีฟ้า,น้ำเงิน", detail: "เป็นกาลกิณีไม่นิยมใช้"},
          ]
        },
        {
          image: require("assets/img/belief/auspiciouscolor/monday.svg"),
          dayTh: "วันจันทร์",
          dayEn: "Monday",
          meaning: [
            {color: "สีขาว,หลือง", detail: "เสริมสร้างบริวาร"},
            {color: "สีชมพู", detail: "อายุยืน เสริมสร้างให้มีสุขภาพที่แข็งแรง"},
            {color: "สีเขียว", detail: "เสริมสร้างให้ดูมีสง่าราศี"},
            {color: "สีม่วง,ดำ", detail: "เสริมสร้างเสน่ห์เมตตาให้คนหลงใหล"},
            {color: "สีส้ม", detail: "เสริมด้านโชคลาภให้ทำมาค้าคล่อง"},
            {color: "สีเทา", detail: "เสริมสร้างจิตให้เข้มแข็ง สร้างความสำเร็จ"},
            {color: "สีฟ้า,น้ำเงิน", detail: "เสริมสร้างเมตาของคนอุปถัมถ์ค้ำชู ช่วยเหลือ"},
            {color: "สีแดง", detail: "เป็นกาลกิณีไม่นิยมใช้"},
          ]
        },
        {
          image: require("assets/img/belief/auspiciouscolor/tuesday.svg"),
          dayTh: "วันอังคาร",
          dayEn: "Tuesday",
          meaning: [
            {color: "สีชมพู", detail: "เสริมสร้างบริวาร"},
            {color: "สีเขียว", detail: "เสริมสร้างให้มีสุขภาพที่แข็งแรง"},
            {color: "สีม่วง,ดำ", detail: "เสริมสร้างให้ดูมีสง่าราศี"},
            {color: "สีส้ม", detail: "เสริมสร้างเสน่ห์เมตตาให้คนหลงใหล"},
            {color: "สีเทา", detail: "เสริมด้านโชคลาภให้ทำมาค้าคล่อง"},
            {color: "สีฟ้า,น้ำเงิน", detail: "เสริมสร้างจิตให้เข้มแข็ง สร้างความสำเร็จ"},
            {color: "สีแดง", detail: "เสริมสร้างเมตาของคนอุปถัมถ์ค้ำชู ช่วยเหลือ"},
            {color: "สีขาว,เหลือง", detail: "เป็นกาลกิณีไม่นิยมใช้"},
          ]
        },
        {
          image: require("assets/img/belief/auspiciouscolor/wednesdaylunch.svg"),
          dayTh: "วันพุธกลางวัน",
          dayEn: "Wednesday Lunch",
          meaning: [
            {color: "สีเขียว", detail: "เสริมสร้างบริวาร"},
            {color: "สีม่วง,ดำ", detail: "เสริมสร้างให้มีสุขภาพที่แข็งแรง"},
            {color: "สีส้ม", detail: "เสริมสร้างให้ดูมีสง่าราศี"},
            {color: "สีเทา", detail: "เสริมสร้างเสน่ห์เมตตาให้คนหลงใหล"},
            {color: "สีฟ้า,น้ำเงิน", detail: "เสริมด้านโชคลาภให้ทำมาค้าคล่อง"},
            {color: "สีแดง", detail: "เสริมสร้างจิตให้เข้มแข็ง สร้างความสำเร็จ"},
            {color: "สีขาว,เหลือง", detail: "เสริมสร้างเมตาของคนอุปถัมถ์ค้ำชู ช่วยเหลือ"},
            {color: "สีชมพู", detail: "เป็นกาลกิณีไม่นิยมใช้"},
          ]
        },
        {
          image: require("assets/img/belief/auspiciouscolor/wednesdaynight.svg"),
          dayTh: "วันพุธกลางคืน",
          dayEn: "Wednesday Night",
          meaning: [
            {color: "สีเทา", detail: "เสริมสร้างบริวาร"},
            {color: "สีฟ้า,น้ำเงิน", detail: "เสริมสร้างให้มีสุขภาพที่แข็งแรง"},
            {color: "สีแดง", detail: "เสริมสร้างให้ดูมีสง่าราศี"},
            {color: "สีขาว,เหลือง", detail: "เสริมสร้างเสน่ห์เมตตาให้คนหลงใหล"},
            {color: "สีชมพู", detail: "เสริมด้านโชคลาภให้ทำมาค้าคล่อง"},
            {color: "สีเขียว", detail: "เสริมสร้างจิตให้เข้มแข็ง สร้างความสำเร็จ"},
            {color: "สีม่วง,ดำ", detail: "เสริมสร้างเมตาของคนอุปถัมถ์ค้ำชู ช่วยเหลือ"},
            {color: "สีส้ม", detail: "เป็นกาลกิณีไม่นิยมใช้"},
          ]
        },
        {
          image: require("assets/img/belief/auspiciouscolor/thursday.svg"),
          dayTh: "วันพฤหัสบดี",
          dayEn: "Thursday",
          meaning: [
            {color: "สีส้ม", detail: "เสริมสร้างบริวาร"},
            {color: "สีเทา", detail: "เสริมสร้างให้มีสุขภาพที่แข็งแรง"},
            {color: "สีฟ้า,น้ำเงิน", detail: "เสริมสร้างให้ดูมีสง่าราศี"},
            {color: "สีแดง", detail: "เสริมสร้างเสน่ห์เมตตาให้คนหลงใหล"},
            {color: "สีขาว,เหลือง", detail: "เสริมด้านโชคลาภให้ทำมาค้าคล่อง"},
            {color: "สีชมพู", detail: "เสริมสร้างจิตให้เข้มแข็ง สร้างความสำเร็จ"},
            {color: "สีเขียว", detail: "เสริมสร้างเมตาของคนอุปถัมถ์ค้ำชู ช่วยเหลือ"},
            {color: "สีม่วง,ดำ", detail: "เป็นกาลกิณีไม่นิยมใช้"},
          ]
        },
        {
          image: require("assets/img/belief/auspiciouscolor/friday.svg"),
          dayTh: "วันศุกร์",
          dayEn: "Friday",
          meaning: [
            {color: "สีฟ้า,น้ำเงิน", detail: "เสริมสร้างบริวาร"},
            {color: "สีแดง", detail: "เสริมสร้างให้มีสุขภาพที่แข็งแรง"},
            {color: "สีขาว,เหลือง", detail: "เสริมสร้างให้ดูมีสง่าราศี"},
            {color: "สีชมพู", detail: "เสริมสร้างเสน่ห์เมตตาให้คนหลงใหล"},
            {color: "สีเขียว", detail: "เสริมด้านโชคลาภให้ทำมาค้าคล่อง"},
            {color: "สีม่วง,ดำ", detail: "เสริมสร้างจิตให้เข้มแข็ง สร้างความสำเร็จ"},
            {color: "สีส้ม", detail: "เสริมสร้างเมตาของคนอุปถัมถ์ค้ำชู ช่วยเหลือ"},
            {color: "สีเทา", detail: "เป็นกาลกิณีไม่นิยมใช้"},
          ]
        },
        {
          image: require("assets/img/belief/auspiciouscolor/saturday.svg"),
          dayTh: "วันเสาร์",
          dayEn: "Saturday",
          meaning: [
            {color: "สีม่วง,ดำ", detail: "เสริมสร้างบริวาร"},
            {color: "สีส้ม", detail: "เสริมสร้างให้มีสุขภาพที่แข็งแรง"},
            {color: "สีเทา", detail: "เสริมสร้างให้ดูมีสง่าราศี"},
            {color: "สีฟ้า,น้ำเงิน", detail: "เสริมสร้างเสน่ห์เมตตาให้คนหลงใหล"},
            {color: "สีแดง", detail: "เสริมด้านโชคลาภให้ทำมาค้าคล่อง"},
            {color: "ขาว,เหลือง", detail: "เสริมสร้างจิตให้เข้มแข็ง สร้างความสำเร็จ"},
            {color: "สีชมพู", detail: "เสริมสร้างเมตาของคนอุปถัมถ์ค้ำชู ช่วยเหลือ"},
            {color: "สีเขียว", detail: "เป็นกาลกิณีไม่นิยมใช้"},
          ]
        },
      ]
    }
  }
}
</script>

<style scoped>

.colorCode {
  color: #be977a;
}


/*iphone5/se*/
@media only screen and (max-width: 320px) {
  .row {
    margin-left: 1rem;
    margin-right: 1rem;
  }

  .col-md-6 {
    margin-top: 2rem;
  }

  .pt-3 {
    margin-left: 2rem;
    margin-right: 2rem;
  }

  .col-sm {
    padding: 0;
  }

  .imgColor {
    object-fit: cover;
    width: 100%;
    padding: 3rem;
  }

  .imgDay {
    width: 60%;
    padding: 0rem;
  }

  .topicDay {
    padding-top: 0rem;
    color: #737d75;
  }

  .details {
    text-align: left;
    padding: 0rem;

  }

  .codeColor {
    font-size: 1.1rem;
  }
}

/*Galaxys5*/
@media only screen and (min-width: 360px) {
  .row {
    margin-left: 1rem;
    margin-right: 1rem;
  }

  .col-md-6 {
    margin-top: 2rem;
  }

  .pt-3 {
    margin-left: 2rem;
    margin-right: 2rem;
  }

  .col-sm {
    padding: 0;
  }

  .imgColor {
    object-fit: cover;
    width: 100%;
    padding: 3rem;
  }

  .imgDay {
    width: 60%;
    padding: 0rem;
  }

  .topicDay {
    padding-top: 0rem;
    color: #737d75;
  }

  .details {
    text-align: left;
    padding: 0rem;

  }

  .codeColor {
    font-size: 1.1rem;
  }
}

/*iphone 6/7/8*/
@media only screen and (min-width: 375px) {
  .pt-3 {
    margin-left: 2rem;
    margin-right: 2rem;
  }

  .col-sm {
    padding: 0;
  }

  .imgColor {
    object-fit: cover;
    width: 100%;
    padding: 2rem;
  }

  .imgDay {
    width: 60%;
    padding: 0rem;
  }

  .topicDay {
    padding-top: 0rem;
    color: #737d75;
  }

  .details {
    text-align: left;
    padding: 0rem;

  }

  .codeColor {
    font-size: 1.1rem;
  }
}

/*I678plus*/
@media only screen and (min-width: 414px) {
  .pt-3 {
    margin-left: 2rem;
    margin-right: 2rem;
  }

  .col-sm {
    padding: 0;
  }

  .imgColor {
    object-fit: cover;
    width: 100%;
    padding: 2rem;
  }

  .imgDay {
    width: 60%;
    padding: 0rem;
  }

  .topicDay {
    padding-top: 0rem;
    color: #737d75;
  }

  .details {
    text-align: left;
    padding: 0rem;

  }

  .codeColor {
    font-size: 1.1rem;
  }

}

/*surfaceDuo*/
@media only screen and (min-width: 540px) {
  .row {
    margin-top: 5rem;
    margin-left: 1rem;
    margin-right: 1rem;
  }

  .col-md-6 {
    margin-top: 2rem;
  }

  .pt-3 {
    margin-left: 2rem;
    margin-right: 2rem;
  }

  .col-sm {
    padding: 0;
  }

  .imgColor {
    object-fit: cover;
    width: 100%;
    padding: 3rem;
  }

  .imgDay {
    width: 60%;
    padding: 0rem;
  }

  .topicDay {
    padding-top: 0rem;
    color: #737d75;
  }

  .details {
    text-align: left;
    padding: 0rem;

  }

  .codeColor {
    font-size: 1.1rem;
  }
}

/*ipad*/
@media only screen and (min-width: 768px) {
  .pt-3 {
    margin-left: 4rem;
    margin-right: 4rem;
  }

  .col-sm {
    padding: 0;
  }

  .col-sm-9 {
    padding-left: 5rem;
    padding-right: 5rem;
  }

  .imgColor {
    object-fit: cover;
    width: 100%;
    padding: 0rem;
  }

  .imgDay {
    width: 50%;
    padding: 0rem;
  }

  .topicDay {
    padding-top: 0;
    color: #737d75;
  }

  .details {
    text-align: left;
    padding: 0px;

  }

  .codeColor {
    font-size: 1.1rem;
  }
}

/*ipadPro*/
@media only screen and (min-width: 1024px) {
  .pt-3 {
    margin-left: 4rem;
    margin-right: 4rem;
  }

  .col-sm {
    padding: 0;
  }

  .col-sm-9 {
    padding-left: 5rem;
    padding-right: 5rem;
  }

  .imgColor {
    object-fit: cover;
    width: 100%;
    padding: 0rem;
  }

  .imgDay {
    width: 100%;
    padding: 0rem;
  }

  .topicDay {
    padding-top: 0;
    color: #737d75;
  }

  .details {
    text-align: left;
    padding: 0rem;

  }

  .codeColor {
    font-size: 1.1rem;
  }

}

/*pc*/
@media only screen and (min-width: 1024px) {
  .pt-3 {
    margin-left: 9rem;
    margin-right: 9rem;
    line-height: 1.6;
  }

  .col-sm {
    padding: 0;
  }

  .imgColor {
    object-fit: cover;
    width: 100%;
    padding-bottom: 5rem;
    padding-top: 5rem;
    padding-left: 15rem;
    padding-right: 15rem;
  }

  .imgDay {
    width: 100%;
    padding: 0rem;
  }

  .topicDay {
    padding-top: 3rem;
    color: #737d75;
  }

  .details {
    text-align: left;
    padding: 0rem;

  }

  .codeColor {
    font-size: 1.1rem;
  }

}

</style>
