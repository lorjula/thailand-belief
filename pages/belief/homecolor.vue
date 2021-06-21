<template>
  <div style="background-color:#F7F6F4;">

    <div style="background-color: #ffffff;">

      <Navbar/>

      <div class="">
        <div class="row">
          <div class="col-sm">
            <img class="imgColor" src="~assets/img/belief/homecolor/cover2.jpg">
          </div>
        </div>
      </div>
    </div>

    <div class="" style="background-color:#F7F6F4; margin-bottom: 9rem;">
      <div class="container" style="text-align: center;">
        <div class="" style="padding-top: 6rem;">
          <h2 style="color: #A0826A;">สีบ้านประจำวันเกิด สร้างสมดุลเสริมมงคล </h2>
          <h5 class="pt-3" style="color: #797979;">
            “บ้าน” คือ สิ่งสำคัญที่สุดอย่างหนึ่งในชีวิต ที่เราและครอบครัวต้องใช้ชีวิตอยู่ไปจนแก่จนเฒ่า จนชั่วลูกชั่วหลาน
            การตกแต่งบ้านจึงเป็นเรื่องที่เราต้องใส่ใจในรายละเอียดให้มาก แม้กระทั่งการเลือก สีทาบ้าน
            ให้ถูกโฉลกกับเจ้าของบ้าน เพราะเชื่อว่าจะทำให้คนในบ้านมีความสุข ไม่ทะเลาะเบาะแว้ง นำพาแต่สิ่งดีๆ
            เข้ามาในครอบครัว พาโชคลาภ และความร่ำรวยให้กับคนในบ้าน
            อีกทั้งการเลือกสีบ้านยังส่งเสริมในเรื่องของหน้าที่การงาน และการเงิน ทำให้อยู่แล้วเจริญก้าวหน้ายิ่งๆ ขึ้นไป
          </h5>
        </div>

        <template v-for="item in birthdayColor">
          <div class="row" style="margin-top: 9rem;">
            <div class="col-md-6">
              <img class="imgDay" :src="item.image">
            </div>
            <div class="col-md-6">
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
  name: "homecolor",
  components: {Recommended, Footer, Navbar},
  data() {
    return {
      birthdayColor: [
        {
          image: require("~/assets/img/belief/homecolor/sunday.png"),
          dayTh: "วันอาทิตย์",
          dayEn: "sunday",
          meaning: [
            {
              detail: "สีแดง เพราะจะช่วยส่งเสริมให้คนเกิดวันอาทิตย์ ได้รับความเคารพนับถือ ให้การสนับสนุน ส่งผลถึงอำนาจและความสำเร็จในการปกครอง การเจริญเติบโตก้าวหน้าในเรื่องการงาน และการเงินด้วย"
            },
          ]
        },
        {
          image: require("assets/img/belief/homecolor/monday.png"),
          dayTh: "วันจันทร์",
          dayEn: "Monday",
          meaning: [
            {detail: "สีฟ้าอ่อน อย่างสีเขียวอ่อน สีครีม สีเงิน หรือโทนสีอ่อน เพราะโทนสีอ่อนจะทำให้บ้านรู้สึกผ่อนคลาย ร่มเย็น สบายตา ปลอดโปร่ง และสีโทนอ่อนยังช่วยส่งเสริมทำให้คนเกิดวันจันทร์ ดูน่าค้นหา มีเสน่ห์ น่าสนใจยิ่งขึ้น"},
          ]
        },
        {
          image: require("assets/img/belief/homecolor/tuesday.png"),
          dayTh: "วันอังคาร",
          dayEn: "Tuesday",
          meaning: [
            {
              detail: "สีโทนอ่อน อย่างสีฟ้าอ่อน สีเขียวอ่อน หรือโทนสีเย็นๆ เพราะจะทำให้คนเกิดวันอังคารรู้สึกผ่อนคลาย เวลาอยู่บ้าน ช่วยลดความกระวนกระวาย ทำให้มีสมาธิ และใจเย็นขึ้น"
            },
          ]
        },
        {
          image: require("assets/img/belief/homecolor/wednesday.png"),
          dayTh: "วันพุธกลางวัน",
          dayEn: "Wednesday Lunch",
          meaning: [
            {detail: "สีแสด สีฟ้า สีขาว เพื่อสร้างความรู้สึกสดชื่น กระปรี้กระเปร่า มีความกระตือรือร้น และมีการตื่นตัวอยู่เสมอ ซึ่งตามหลักฮวงจุ้ยจะทำให้บ้านอยู่เย็นเป็นสุข"},
          ]
        },
        {
          image: require("assets/img/belief/homecolor/wednesdaynight.png"),
          dayTh: "วันพุธกลางคืน",
          dayEn: "Wednesday Night",
          meaning: [
            {detail: "สีเขียวอ่อน สีเทา สีขาวนวล สีชมพู สีกลุ่มนี้เป็นโทนสีที่ถูกโฉลกกับคนเกิดวันพุธตอนกลางคืน ช่วยส่งเสริมให้คนในบ้านอยู่เย็นเป็นสุข มีชีวิตที่ดีขึ้น"},
          ]
        },
        {
          image: require("assets/img/belief/homecolor/thursday.png"),
          dayTh: "วันพฤหัสบดี",
          dayEn: "Thursday",
          meaning: [
            {detail: "สีน้ำตาล สีพีช สีส้มอ่อน สีครีม เพราะจะทำให้คนที่เกิดวันพฤหัสบดี รู้สึกสงบ มีความเป็นส่วนตัว มีความปลอดภัย อบอุ่น รู้สึกเหมือนตัดออกจากความวุ่นวายของโลกภายนอก ส่งเสริมทำให้มีความสุขกาย สุขใจ ทำให้บ้านร่มเย็นน่าอยู่"},

          ]
        },
        {
          image: require("assets/img/belief/homecolor/friday.png"),
          dayTh: "วันศุกร์",
          dayEn: "Friday",
          meaning: [
            {detail: "สีเขียวอ่อน สีขาว สีควันบุหรี่ สีส้มอ่อน เพราะจะทำให้คนเกิดวันศุกร์รู้สึกผ่อนคลาย สบาย สงบ เหมือนได้อยู่กับธรรมชาติ ทำให้อารมณ์ดี มีความสุข"},

          ]
        },
        {
          image: require("assets/img/belief/homecolor/saturday.png"),
          dayTh: "วันเสาร์",
          dayEn: "Saturday",
          meaning: [
            {detail: "สีขาว สีควันบุหรี่ สีเขียวอ่อน เพราะจะช่วยระงับความใจร้อนลงได้ และยังทำให้รู้สึกสบาย ผ่อนคลาย ปลอดโปร่ง สบายตา สบายใจ ทำให้บรรยากาศในบ้านเย็นลง เพิ่มความอบอุ่น และช่วยส่งเสริมให้คนบ้านอยู่อย่างสงบสุข สบายใจ"},
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
    margin-left: 2rem;
    margin-right: 2rem;
    line-height: 1.6;

  }
}

/*Galaxys5*/
@media only screen and (min-width: 360px) {
  .pt-3 {
    margin-left: 2rem;
    margin-right: 2rem;
  }
}

/*iphone 6/7/8*/
@media only screen and (min-width: 375px) {
  .pt-3 {
    margin-left: 2rem;
    margin-right: 2rem;
  }
}

/*I678plus*/
@media only screen and (min-width: 414px) {
  .pt-3 {
    margin-left: 2rem;
    margin-right: 2rem;
  }
}

/*surfaceDuo*/
@media only screen and (min-width: 540px) {
  .pt-3 {
    margin-left: 2rem;
    margin-right: 2rem;
  }
}

/*ipad*/
@media only screen and (min-width: 768px) {
  .pt-3 {
    margin-left: 4rem;
    margin-right: 4rem;
  }
}

/*ipadPro*/
@media only screen and (min-width: 1024px) {
  pt-3 {
    margin-left: 4rem;
    margin-right: 4rem;
  }
}

/*pc*/
@media only screen and (min-width: 1024px) {
  .pt-3 {
    margin-left: 9rem;
    margin-right: 9rem;
    line-height: 1.6;
  }

}
</style>
