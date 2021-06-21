<template>
  <div style="background-color:#F7F6F4;">

    <div style="background-color: #f7f6f4;;">

      <Navbar/>

      <div class="container">
        <div class="row">
          <div class="col-sm">
            <img class="imgColor" src="~assets/img/belief/wallet/cover.jpeg" style="border-radius: 4px;">
          </div>
        </div>
      </div>
    </div>

    <div class="" style="background-color:#F7F6F4; margin-bottom: 9rem;">
      <div class="container" style="text-align: center;">
        <div class="" style="padding-top: 6rem;">
          <h2 style="color: #A0826A;">สีกระเป๋าสตางค์ ตามวันเกิด ดูดทรัพย์</h2>
          <h5 class="pt-3" style="color: #797979;">
            ความเชื่อในเรื่องการเลือกใช้กระเป๋าตังค์ เพื่อเสริมเรื่องดวงการเงินที่จะเข้ามา
            เปิดกระเป๋ารับทรัพย์กันเเบบรัวๆ เพียงเเค่เราเลือกสีกระเป๋าตังค์ให้ถูกกับโฉลกวันเกิดของตน
            ใช้แบงค์ขวัญถุงที่ควรพกไว้เรียกเงินในกระเป๋า ใครเกิดวันไหนต้องใช้กระเป๋าสตางค์สีอะไร ไปดูกันเลยค๊า

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
        <a class="dataSource" href="https://horoscope.trueid.net/detail/zgzAxmGWeapX" style="text-decoration:none;">
          <h5>ที่มา: https://horoscope.trueid.net</h5>
        </a>

      </div>

    </div>
    <Recommended/>

    <Footer/>
  </div>
</template>

<script>
import Navbar from "~/components/nav/navbar";
import Recommended from "~/components/belief/recommended";
import Footer from "~/components/footer/footer";

export default {
  name: "wallet",
  components: {Footer, Recommended, Navbar},
  data() {
    return {
      birthdayColor: [
        {
          image: require("~/assets/img/belief/wallet/w1.png"),
          link: {
            to: "https://www.pinterest.com/pin/594545588278560211/",
            display: "www.pinterest.com",
          },
          dayTh: "วันอาทิตย์",
          dayEn: "sunday",
          meaning: [
            {color: "แดง,ชมพู,โอลด์โรส", detail: "ส่งเสริมอำนาจ บารมี"},
            {color: "เหลือง,ขาว,เทา", detail: "ส่งเสริมสุขภาพ"},
            {color: "เขียวอ่อน,เขียวแก่", detail: "ส่งเสริมโชคลาภ"},
            {color: "ดำ,ม่วง,น้ำตาลเข้ม", detail: "ส่งเสริมเงินทอง ทรัพย์สมบัติ "},
            {color: "น้ำเงิน,คราม,ฟ้า", detail: "สีกาลกิณี"},
            {auspicious: " แบงค์ขวัญถุง ธนบัตรใบละ 50 บาท ที่มีเลขลงท้ายด้วย 68 หรือ 86 "},
          ]
        },
        {
          image: require("assets/img/belief/wallet/w2.png"),
          link: {
            to: "https://www.pinterest.com/pin/584271751631969058/",
            display: "www.pinterest.com",
          },
          dayTh: "วันจันทร์",
          dayEn: "Monday",
          meaning: [
            {color: "เหลือง,ขาว,เทา,เขียว", detail: "ส่งเสริมอำนาจ บารมี"},
            {color: "ชมพู,โอลด์โรส", detail: "ส่งเสริมสุขภาพ"},
            {color: "ดำ,ม่วง,น้ำตาลเข้ม", detail: "ส่งเสริมโชคลาภ"},
            {color: "แสด,เหลืองเข้ม,ส้ม,ทอง", detail: "ส่งเสริมเงินทอง ทรัพย์สมบัติ"},
            {color: "แดง ", detail: "สีกาลกิณี"},
            {auspicious: " แบงค์ขวัญถุง ธนบัตรใบละ 20 บาท ที่มีเลขลงท้ายด้วย 56 หรือ 65  "},
          ]
        },
        {
          image: require("assets/img/belief/wallet/w3.png"),
          link: {
            to: "https://www.pinterest.com/pin/803611127261654037/",
            display: "www.pinterest.com",
          },
          dayTh: "วันอังคาร",
          dayEn: "Tuesday",
          meaning: [
            {color: "ชมพู,โอลด์โรส,ดำ,ม่วง,น้ำตาลเข้ม", detail: "ส่งเสริมอำนาจ บารมี"},
            {color: "เขียว", detail: "ส่งเสริมสุขภาพ"},
            {color: "แสด,เหลืองเข้ม,ส้ม,ทอง", detail: "ส่งเสริมโชคลาภ"},
            {color: "เทาเข้ม", detail: "ส่งเสริมเงินทอง ทรัพย์สมบัติ"},
            {color: "เหลืองอ่อน,ขาว", detail: "สีกาลกิณี"},
            {auspicious: " แบงค์ขวัญถุง ธนบัตรใบละ 50 บาท ที่มีเลขลงท้ายด้วย 36 หรือ  63  "},
          ]
        },
        {
          image: require("assets/img/belief/wallet/w4.png"),
          link: {
            to: "https://www.pinterest.com/pin/803611127261652746/",
            display: "www.pinterest.com",
          },
          dayTh: "วันพุธกลางวัน",
          dayEn: "Wednesday Lunch",
          meaning: [
            {color: "เขียว,แสด,เหลืองเข้ม,ส้ม,ทอง ", detail: "ส่งเสริมอำนาจ บารมี"},
            {color: "ดำ,ม่วง,น้ำตาลเข้ม", detail: "ส่งเสริมสุขภาพ"},
            {color: "เทาเข้ม ", detail: "ส่งเสริมโชคลาภ"},
            {color: "น้ำเงิน,คราม,ฟ้า   ", detail: "ส่งเสริมเงินทอง ทรัพย์สมบัติ"},
            {color: "ชมพู,โอลด์โรส", detail: "สีกาลกิณี"},
            {auspicious: " แบงค์ขวัญถุง "},

          ]
        },
        {
          image: require("assets/img/belief/wallet/w5.png"),
          link: {
            to: "https://www.pinterest.com/pin/803611127261652768/",
            display: "www.pinterest.com",
          },
          dayTh: "วันพุธกลางคืน",
          dayEn: "Wednesday Night",
          meaning: [
            {color: "เทาเข้ม,แดง ", detail: "ส่งเสริมอำนาจ บารมี"},
            {color: "น้ำเงิน,คราม,ฟ้า", detail: "ส่งเสริมสุขภาพ"},
            {color: "เหลืองอ่อน,ขาว,เทา", detail: "ส่งเสริมโชคลาภ"},
            {color: "ชมพู,โอลด์โรส  ", detail: "ส่งเสริมเงินทอง ทรัพย์สมบัติ"},
            {color: "แสด,เหลืองเข้ม,ส้ม,ทอง ", detail: "สีกาลกิณี"},
            {auspicious: " แบงค์ขวัญถุง ธนบัตรใบละ 20 บาท ที่มีเลขลงท้ายด้วย 15 หรือ  51 "},
          ]
        },
        {
          image: require("assets/img/belief/wallet/w6.png"),
          link: {
            to: "https://www.pinterest.com/pin/528047125044513585/",
            display: "www.pinterest.com",
          },
          dayTh: "วันพฤหัสบดี",
          dayEn: "Thursday",
          meaning: [
            {color: "แสด,เหลืองเข้ม,ส้ม,ทอง,น้ำเงิน,คราม,ฟ้า", detail: "ส่งเสริมอำนาจ บารมี"},
            {color: "เทาเข้ม ", detail: "ส่งเสริมสุขภาพ"},
            {color: "แดง", detail: "ส่งเสริมโชคลาภ"},
            {color: "เหลืองอ่อน,ขาว,เทา", detail: "ส่งเสริมเงินทอง ทรัพย์สมบัติ"},
            {color: "ดำ,ม่วง,น้ำตาลเข้ม ", detail: "สีกาลกิณี"},
            {auspicious: " แบงค์ขวัญถุง ธนบัตรใบละ 100 บาท ที่มีเลขลงท้ายด้วย 56 หรือ  65"},
          ]
        },
        {
          image: require("assets/img/belief/wallet/w7.png"),
          link: {
            to: "https://www.pinterest.com/pin/803611127261654025/",
            display: "www.pinterest.com",
          },
          dayTh: "วันศุกร์",
          dayEn: "Friday",
          meaning: [
            {color: "น้ำเงิน,คราม,ฟ้า,เหลือง,ขาว,เทา", detail: "ส่งเสริมอำนาจ บารมี"},
            {color: "แดง", detail: "ส่งเสริมสุขภาพ"},
            {color: "ชมพู,โอลด์โรส", detail: "ส่งเสริมโชคลาภ"},
            {color: "เขียว", detail: "ส่งเสริมเงินทอง ทรัพย์สมบัติ"},
            {color: "เทาเข้ม ", detail: "สีกาลกิณี"},
            {auspicious: " แบงค์ขวัญถุง ธนบัตรใบละ 100 บาท ที่มีเลขลงท้ายด้วย 69 หรือ  96"},
          ]
        },
        {
          image: require("assets/img/belief/wallet/w8.png"),
          link: {
            to: "https://www.pinterest.com/pin/803611127261654000/",
            display: "www.pinterest.com",
          },
          dayTh: "วันเสาร์",
          dayEn: "Saturday",
          meaning: [
            {color: "ดำ,ม่วง,น้ำตาลเข้ม,เทาเข้ม", detail: "ส่งเสริมอำนาจ บารมี"},
            {color: "แสด,เหลืองเข้ม,ส้ม,ทอง", detail: "ส่งเสริมสุขภาพ"},
            {color: "น้ำเงิน,คราม,ฟ้า", detail: "ส่งเสริมโชคลาภ"},
            {color: "แดง", detail: "ส่งเสริมเงินทอง ทรัพย์สมบัติ"},
            {color: "เขียว", detail: "สีกาลกิณี"},
            {auspicious: " แบงค์ขวัญถุง ธนบัตรใบละ 20 บาท ที่มีเลขลงท้ายด้วย 89 หรือ  98"},
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
