<template>
  <div style="background-color:#F7F6F4;">

    <div style="background-color: #ffffff;">

      <Navbar/>

      <div class="">
        <div class="row">
          <div class="col-sm">
            <img class="imgColor" src="~assets/img/belief/tree/cover.jpg">
          </div>
        </div>
      </div>
    </div>

    <div class="" style="background-color:#F7F6F4; margin-bottom: 9rem;">
      <div class="container" style="text-align: center;">
        <div class="" style="padding-top: 6rem;">
          <h2 style="color: #A0826A;">ต้นไม้มงคล ประจำวันเกิด </h2>
          <h5 class="pt-3" style="color: #797979;">
            การเลือกต้นไม้มาปลูกที่บ้านก็มีส่วนสำคัญเช่นกัน การที่เราจะนำต้นไม้มาปลูกให้เหมาะกับสภาพอากาศ
            ดินที่บ้านของเราเเล้ว
            อีกทั้งถ้าเราเลือกนำต้นไม้มงคลที่เหมาะกับดวงวันเกิดเขาเชื่อกันว่าจะนำพาสิ่งดีๆมาให้คนที่อาศัยอยู่ในบ้าน
            ทั้งเสริมด้านการงาน ด้านการเงิน สุขภาพเเละความรัก นอกจากจะได้สวนสวยร่มรื่น ยังได้ความร่มเย็นเป็นสุขตามมาด้วย
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
                            <td class="colorCode">{{ m.tree }}</td>
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
                        <table style="margin: 0;">
                          <template v-for="m in item.meaning">
                            <tr>{{ m.limitation }}</tr>
                          </template>
                        </table>
                      </div>
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
import Recommended from "~/components/belief/recommended";
import Footer from "~/components/footer/footer";

export default {
  name: "tree",
  components: {Footer, Recommended, Navbar}
  ,
  data() {
    return {
      birthdayColor: [
        {
          image: require("~/assets/img/belief/tree/t1.png"),
          link: {
            to: "https://twitter.com/flower_posts/status/1361262234933018629?s=12",
            display: "twitter.com",
          },
          dayTh: "วันอาทิตย์",
          dayEn: "sunday",
          meaning: [
            {tree: "กุหลาบ", detail: "ทำให้ชีวิตมสง่างามมีราศี จะเกิดสิ่งภาคภูมิให้จัวเราเอง"},
            {tree: "โป๊ยเซียน", detail: "เลือกปลูกสีส้มหรือสีเหลือง จะนำโชคลาภเข้ามาหาเราเสมอ"},
            {tree: "ราชพฤกษ์", detail: "เสริมให้มีเกียรติยศ มีศักดิ์ศรีมีคนเคารพนับถือ"},
            {tree: "จำปา", detail: "ช่วยนำโชค ให้กับคนวที่ันอาทิตย์เป็นอย่างมาก"},
            {tree: "โกสน", detail: "จะช่วยคุ้มครองให้บ้านอยู่เย็นเป็นสุข"},
            {auspicious: "ไม้มงคลของคนเกิดวันอาทิตย์ จะเป็นไม้ดอกสีเหลือง หรือสีส้ม เป็นสีที่ถูกโฉลกเป็นสิริมงคลของคนเกิดวันอาทิตย์"},
            {limitation: "คนเกิดวันอาทิตย์ควรระวัง คือ เรื่องความใจร้อน เรื่องความหูเบาเชื่อคนง่าย และเรื่องหน้าใหญ่ใจโต ซึ่งอาจจะสร้างศัตรูโดยไม่รู้ตัว"},
          ]
        },
        {
          image: require("assets/img/belief/tree/t2.png"),
          link: {
            to: "https://www.pinterest.com/pin/560205641139033589/",
            display: "www.pinterest.com",
          },
          dayTh: "วันจันทร์",
          dayEn: "Monday",
          meaning: [
            {tree: "มะลิ", detail: "เสริมสิริมงคลให้คนในบ้านมีความบริสุทธิ์ เอิมอิ่ม มีคนเอ็นดูรักใคร่ "},
            {
              tree: "วาสนา",
              detail: " วาสนาราชินี จะให้บุญสูง วาสนาอธิษฐานจะทำให้สมหวังดั่งใจหรือจะเป็นวาสนาชนิดอื่นก็ได้ผลดีทั้งสิ้น"
            },
            {tree: "โป๊ยเซียน", detail: "ปลูกโป๊ยเซียนสีเหลือง หรือสีขาว จะช่วยให้มีโชคลาภเข้ามาบ่อยๆ "},
            {tree: "จำปี", detail: "เสริมให้ชีวิตรุ่งเรืองรุ่งโรจน์ และหน้าที่การงานเจริญก้าวหน้า "},
            {tree: "กวนอิม", detail: "ให้โชคด้านการเงิน มีฐานะร่ำรวย ไม่ลำบาก"},
            {tree: "มะม่วง", detail: "ช่วยเสริมให้ผู้ปลูกและผู้อาศัยมีเงินทองเหลือเก็บเหลือใช้"},
            {tree: "พลูด่าง", detail: "ช่วยให้ชีวิตเจริญงอกงาม"},
            {tree: "แก้ว", detail: "ส่งผลให้คนในบ้านมีจิตใจแจ่มใส มีความสุขทางกายและใจ"},
            {
              tree: "มะยม",
              detail: "ปกป้องความชั่วร้าย และเรื่องไม่ดีเข้ามาเกี่ยวกับคนมนบ้าน และเสริมให้มีผู้นิยมชมชอบ"
            },
            {auspicious: "ต้นไม้มงคลสำหรับคนเกิดวันจันทร์ ถ้าเป็นไม้ดอกควรเป็นไม้ที่มีดอกสีขาวหรือเหลืองจะถูกโฉลกมาก คนเกิดวันจันทร์จะมีต้นไม้มงคลให้เลือกปลูก"},
            {limitation: "คนเกิดวันจันทร์ ควรลดความ วิตกกังวลลงบ้าง ให้ระวังการคบคนไม่ดีจะนำเรื่องเดือดร้อนมาให้ หรือเสียโอกาสในการก้าวหน้า และให้ระวังการใช้จ่าย อย่าตามใจตัวเอง ซึ่งอาจจะสร้างศัตรูโดยไม่รู้ตัว"},

          ]
        },
        {
          image: require("assets/img/belief/tree/t3.png"),
          link: {
            to: "https://www.pinterest.com/pin/503910645814580583/",
            display: "www.pinterest.com",
          },
          dayTh: "วันอังคาร",
          dayEn: "Tuesday",
          meaning: [
            {tree: "โป๊ยเซียน", detail: "จะเจอเเต่ความโชคดีในชีวิตอยู่เสมอ "},
            {tree: "กุหลาบ", detail: " ความเจริญรุ่งเรืองในชีวิต สุขกายดี สบายใจ มีความภาคภูมิ"},
            {tree: "เข็ม", detail: " ทำให้สมองปลอดโปร่ง มีความคิดความอ่านสร้างสรรค์ที่ดี"},
            {tree: "ชบา", detail: " ความเจริญก้าวหน้า ทำให้ไม่มีปัญหาและอุปสรรคในการดำเนินชีวิต"},
            {tree: "โกสน", detail: "เสริมคุณงามความดี สร้างบุญให้ชีวิต"},
            {tree: "พญายอ", detail: "ช่วยให้การดำเนินชีวิตราบรื่น สมบูรณ์เเบบมีแต่ความสุข"},
            {auspicious: "ต้นไม้มงคลสำหรับคนเกิดวันอังคาร สีมงคลของคนวันอังคารคือ สีแดง หรือชมพู"},
            {limitation: "คนเกิดวันอังคาร ควรระวังเรื่องใจร้อน จะทำให้ชีวิตไม่ประสบความสำเร็จ ควรมีความยับยั้งชั่งใจในการใช้จ่าย ควรมีการวางแผนในชีวิตให้ดี"},
          ]
        },
        {
          image: require("assets/img/belief/tree/t4.png"),
          link: {
            to: "https://www.pinterest.com/pin/607000856011385948/",
            display: "www.pinterest.com",
          },
          dayTh: "วันพุธกลางวัน",
          dayEn: "Wednesday Lunch",
          meaning: [
            {tree: "โป๊ยเซียน", detail: "จะนำโชคลาภมาให้ จะได้โชคลาภแบบฟลุกๆ "},
            {tree: "วาสนา", detail: "คิดสิ่งใดก็สมปรารถนา สมหวังดั่งใจคิด "},
            {tree: "กล้วย", detail: "ทำให้คนที่อยู่ในบ้านอยู่เย็นเป็นสุข มีความสุขกายสบายใจ "},
            {tree: "ราชพฤกษ์", detail: "เสริมด้านชื่อเสียง เกียรติยศ ศักดิ์ศรี "},
            {tree: "กุหลาบ", detail: "หากปลูกกุหลาบสีเหลือง จะช่วยให้มีความสุขสมบูรณ์ในทุก ๆ ด้าน"},
            {tree: "โกสน", detail: "เสริมคุณงามความดี สร้างบุญให้ชีวิต"},
            {tree: "พลูด่าง", detail: "ส่งเสริมให้มีความเจริญงอกงามในชีวิต"},
            {auspicious: "ต้นไม้มงคลที่ควรปลูก คือ ดอกไม้ที่มีสีเหลือง เนื่องจากเป็นสีที่ถูกโฉลก จะช่วยเสริมสิ่งดี ๆ ให้กับชีวิต"},
            {limitation: "วันพุธกลางวัน ควรระมัดระวังเรื่องใจอ่อนใจง่ายเชื่อคนง่าย และความใจกว้างจนเกินไป"},
          ]
        },
        {
          image: require("assets/img/belief/tree/t5.png"),
          link: {
            to: "https://www.pinterest.com/pin/530017449892560948/",
            display: "www.pinterest.com",
          },
          dayTh: "วันพุธกลางคืน",
          dayEn: "Wednesday Night",
          meaning: [
            {tree: "โป๊ยเซียน", detail: "ปลูกแล้วจะนำโชคลาภมาให้ผู้ปลูกและคนในครอบครัว "},
            {tree: "วาสนา", detail: "เกิดความสุขสมหวังดั่งใจปรารถนา คิดสิ่งใดก็ได้สิ่งนั้น "},
            {tree: "กล้วย", detail: "ทำให้บ้านร่มเย็นเป็นสุข ผู้ปลูกสุขกายสบายใจ "},
            {tree: "ราชพฤกษ์", detail: "เสริมด้านชื่อเสียง เกียรติยศ ศักดิ์ศรี "},
            {tree: "กุหลาบ", detail: "หากปลูกกุหลาบสีเหลือง จะช่วยให้มีความสุขสมบูรณ์ในทุก ๆ ด้าน"},
            {tree: "โกสน", detail: "ช่วยสร้างบุญ เพิ่มคุณงามความดี ให้ร่มเย็นเป็นสุข"},
            {tree: "พลูด่าง", detail: "ส่งเสริมให้มีความเจริญงอกงามในชีวิต"},
            {auspicious: "ต้นไม้มงคลที่ควรปลูก คือ ต้นไม้สีเหลือง หรือต้นที่มีดอกไม้สีเหลือง เช่นเดียวกับคนเกิดวันพุธกลางวัน"},
            {limitation: "คนที่เกิดวันพุธกลางคืน จะเป็นคนดื้อรัน ไม่ฟังใคร ไม่ชอบเเก้ไขปรับปรุงตัวเอง มักชอบเชื่อคนที่ไม่จริงใจกับตนฐานะลุ่มๆ ดอนๆ มีเงินแต่ไม่พอใช้จ่าย มีความรู้ความสามารถ มีความตั้งใจสูง แต่ไม่ค่อยประสบความสำเร็จเหมาะกับการประกอบอาชีพครูสอนศีลธรรม หรือวิชาช่างจึงจะดี จะตั้งตัวได้เมื่ออายุมากแล้ว"},
          ]
        },
        {
          image: require("assets/img/belief/tree/t6.png"),
          link: {
            to: "https://www.pinterest.com/pin/528047125044513585/",
            display: "www.pinterest.com",
          },
          dayTh: "วันพฤหัสบดี",
          dayEn: "Thursday",
          meaning: [
            {tree: "มะลิ", detail: "เสริมสิริมงคลให้คนในบ้านมีความบริสุทธิ์ เอิมอิ่ม มีคนเอ็นดูรักใคร่ "},
            {tree: "จำปี", detail: "จะช่วยเสริมเรื่องหน้าที่การงานให้เจริญก้าวหน้า มั่งคง"},
            {tree: "กุหลาบ", detail: "เลือกปลูกดอกสีขาว จะช่วยเสริมในเรื่องความสง่าราศี ผู้คนนับหน้าถือตา"},
            {tree: "พุด", detail: "ส่งผลให้ผู้ปลูกและคนในบ้านมีความแข็งแรง สมบูรณ์ เจริญมั่นคง"},
            {tree: "กุหลาบ", detail: "ควรเป็นดอกสีขาว หากนำมาปลูกเลี้ยงไว้จะทำให้เกิดความสง่างาม ภาคภูมิ"},
            {
              tree: "แก้ว",
              detail: "ท่านว่าปลูกแล้วจะส่งผลให้คนในบ้านนั้นมีความดี มีความสูงค่ามีจิตใจแจ่มใสบริสุทธิ์ดุจแก้ว"
            },
            {auspicious: "ต้นไม้มงคลที่ควรปลูก คือ ต้นไม้หรือดอกไม้ที่มีสีขาว จะเสริมดวงให้แก่คนเกิดวันพฤหัสบดี"},
            {limitation: "ชะตาชีวิตจะได้ดีมี เกียรติ มีทรัพย์สมบัติ แต่จะมีทุกข์เรื่องเพื่อนฝูงหรือคู่ครอง เพราะเป็นคนเจ้าชู้ บริวารไม่ค่อยเชื่อฟัง ชะตาชีวิตต้อยคอยค้ำชูผู้อยู่รอบข้างเสมอ"},
          ]
        },
        {
          image: require("assets/img/belief/tree/t7.png"),
          link: {
            to: "https://www.pinterest.com/pin/455215474813632435/",
            display: "www.pinterest.com",
          },
          dayTh: "วันศุกร์",
          dayEn: "Friday",
          meaning: [
            {tree: "เข็ม", detail: "ทำให้ชีวิตก้าวหน้า และเดินไปในทางที่ดี "},
            {tree: "กุหลาบ", detail: "ควรปลูกกุหลาบสีแดง จะทำให้เกิดความสง่า และเกิดความภาคภูมิใจ "},
            {tree: "โกสน", detail: "ช่วยสร้างบุญ เพิ่มคุณงามความดี ให้ร่มเย็นเป็นสุข "},
            {tree: "โป๊ยเซียน", detail: "จะทำให้มีโชคลาภ มีข่าวดีเกี่ยวกับเรื่องเงินทอง "},
            {tree: "อัญชัน", detail: "เสริมให้มีการประสบความสำเร็จในชีวิต"},
            {auspicious: "ต้นไม้มงคลที่ควรปลูก คือ ดอกไม้สีแดงหรือสีชมพู"},
            {limitation: "ชะตาชีวิตมักถูกคนรอบข้าง เบียดเบียนพึ่งพาอาศัย แต่ตัวเองก็ยินดีช่วย ต้องทำงานที่ใช้พรสวรรค์จะได้ดีกว่าทางที่เล่าเรียนมา จะอาภัพคู่ครอง เป็นคนเจ้าชู้หมกมุ่นในโลกีย์ โดยทั่วไปมักไม่ตกยาก เพราะมีความรู้ดีและมีผู้ใหญ่ให้ความเอ็นดูอยู่เสมอ ให้ระวังเรื่องความใจอ่อน และไม่ควรวางใจใครง่ายๆ"},

          ]
        },
        {
          image: require("assets/img/belief/tree/t8.png"),
          link: {
            to: "https://www.pinterest.com/pin/406661041343873163/",
            display: "www.pinterest.com",
          },
          dayTh: "วันเสาร์",
          dayEn: "Saturday",
          meaning: [
            {tree: "วาสนา", detail: "เกิดแรงบันดาลใจ เกิดความสุขความสมหวัง สมปรารถนา "},
            {tree: "กวนอิม", detail: "จะมีฐานะดี มีความร่ำรวย มีเงินทอง "},
            {tree: "จำปี", detail: "เสริมให้ประสบความสำเร็จในชีวิตการงาน มีความเจริญก้าวหน้า "},
            {tree: "มะม่วง", detail: "นอกจากจะให้ผลไว้กินแล้ว ยังทำให้ผู้ปลูกร่ำรวยยิ่งขึ้นด้วย "},
            {tree: "ชมพู่", detail: "ทำให้ชีวิตเจริญรุ่งเรือง การงานก้าวหน้า"},
            {tree: "ราชพฤกษ์หรือคูน", detail: "มีความเป็นมงคลทางด้านช่วยให้มีเกียรติและมีศักดิ์ศรี"},
            {auspicious: "ต้นไม้มงคลที่ควรปลูก คือ ต้นไม้ที่เสริมโชคลาภวาสนาให้กับคนเกิดวันเสาร์"},
            {limitation: "ชะตาชีวิตชอบอยู่อย่าง เรียบง่าย ชอบงานที่ไม่ต้องเคร่งเครียด มักมีคู่มากแต่ไม่ใช่คู่แท้ ควรระวังเรื่องเพื่อนจะนำความเดือดร้อนมาให้ และหากเชื่อฟังคำเตือนของคนอื่นบ้าง ลดความห้าวหาญลงบ้างจะได้ดีมีอนาคตสดใส"},
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
