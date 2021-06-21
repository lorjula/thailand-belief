<template>
  <div style="background-color:#F7F6F4;">

    <div style="background-color: #ffffff;">

      <Navbar/>

    </div>

    <div class="" style="background-color:#F7F6F4; margin-bottom: 9rem;">
      <div class="container" style="text-align: center;">
        <div class="" style="padding-top: 6rem;">
          <h2 style="color: #A0826A;">วัดนาคปรก</h2>
          <h5 class="pt-3" style="color: #797979;margin-left:4rem;margin-right: 4rem;line-height: 1.6;">
            วัดนาคปรก เป็นวัดประจำของเราเอง เเต่ก่อนอื่นเรามารู้จักกับวัดนาคปรกกันคร่าวๆกันก่อน
            ซึ่งตามประวัติสมัยอยุธยาตอนปลาย-กรุงรัตนโกสินทร์ตอนต้น (รัชกาลที่ ๓-๔)
            มีพ่อค้าเรือสำเภาชาวจีน ชื่อ พระบริบูรณ์ธนากร (เจ้าสัวพุก แซ่ตัน) เดินทางมาที่พระนคร เจ้าสัวพุก
            เป็นผู้มีศรัทธาเลื่อมใสในพระพุทธศาสนา ได้คิดริเริ่มก่อสร้างวัดขึ้น
            เพื่อใช้เป็นสถานที่ประกอบพิธีกรรม กิจกรรม และศาสนกิจทางพระพุทธศาสนา
            และตอบแทนชาวไทยที่ทำให้การค้าขายของตนเติบโต</h5>
        </div>

        <template v-for="item in monastery">
          <div class="row " style="margin-top: 9rem;">
            <div class="col-md-4"></div>
            <div class="col-md-4">
              <img style="object-fit: cover;width:100%;"
                   :src="item.image">
            </div>
            <div class="col-md-4"></div>

          </div>

          <div class="row" style="margin-top: 5rem;">
            <div class="col-md">
              <h5 class="pt-3" style="color: #797979;margin-left:4rem;margin-right: 4rem;line-height: 1.6;">
                {{ item.content }}
              </h5>
            </div>
          </div>
        </template>

        <div style="margin-top: 3rem;">
          <h3 data-v-4095699c="" class="temple" style="padding-top: 2rem;">ภาพรวม "วัดนาคปรก"</h3>
        </div>

        <div class="row" style="margin-top: 5rem;">
          <template v-for="item in photoAll">
            <div class="col-md-3" style="padding: 1rem;">
              <img class="w-100" :src="item.image">
            </div>
          </template>
        </div>

        <a class="dataSource" href="https://www.facebook.com/papaiwatofficial/posts/1012538735580201"
           style="text-decoration:none; ">
          <h6 style=" margin-top: 5rem; width: 100%;">
            ขอบคุณข้อมูล:papaiwatofficial</h6>
        </a>

      </div>
    </div>

    <Map :map="map" :day="day"/>

    <RecommenBangkok/>

    <Footer/>
  </div>
</template>

<script>
import Navbar from "~/components/nav/navbar";
import Footer from "~/components/footer/footer";
import Map from "~/components/monastery/map";
import RecommenBangkok from "~/components/monastery/recommen/recommenBangkok";

export default {
  name: "nakprong",
  components: {RecommenBangkok, Map, Footer, Navbar},
  data() {
    return {
      map: {
        link: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3876.0199136311994!2d100.46461461446339!3d13.717243701789915!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x30e298419954fe3d%3A0x21c04e6ca41cb296!2sWat%20Nak%20Prok!5e0!3m2!1sen!2sth!4v1623592268831!5m2!1sen!2sth",
        address: "99 ถนนเทอดไท แขวง ปากคลองภาษีเจริญ เขตภาษีเจริญ กรุงเทพมหานคร 10160"
      },
      day: {
        sunday: "08.00-18.00 น.",
        monday: "08.00-18.00 น.",
        tuesday: "08.00-18.00 น.",
        wednesday: "08.00-18.00 น.",
        thursday: "08.00-18.00 น.",
        friday: "08.00-18.00 น.",
        saturday: "08.00-18.00 น.",
      },
      monastery: [
        {
          image: require("~/assets/img/monastery/nakprok/n1.jpg"),
          content: "ด้านในพระวิหาร มีองค์พระประธาน มีนามว่า (หลวงพ่อนาคปรก) เป็นพระพุทธรูปปางมารวิชัยมาจากเมืองสุโขทัย มีพญานาค ๗ เศียรแผ่พังพาน เป็นรูปปูนปั้นองค์พระเป็นพระปางมารวิชัยสัมฤทธิ์ ชาวบ้านจึงได้เรียกว่า “วัดนาคปรก” ซึ่งวัดนาคปรกนั้นเราจะพบพระพุทธรูปปางต่างๆแต่ที่มีความพิเศษก็คือแต่ละองค์นั้นจะมีพญานาคปรกที่พระพุทธรูปทุกองค์"
          ,

        },
        {
          image: require("~/assets/img/monastery/nakprok/n2.jpg"),
          content: "ในด้านขวามือก่อนเข้าไปในวิหารนั้น จะมีพระนาคปรกไม้ตะเคียน เเละ พระอุปคุตมหาเถระ ที่เเกะสลักจากไม้ตะเคียน อายุ 500 ปี อยู่ ซึ่งจะมีประชาชนมากราบไหว้ขอพรกันเป็นจำนวนมาก ",
        },
        {
          image: require("~/assets/img/monastery/nakprok/n3.jpg"),
          content: "ทุกครั้งที่เรามาวัดนาคปรกเเห่งนี้ เราจะไปไหว้ของพร พ่อปู่หมอชีวก โกมารภัจจ์ ทุกครั้ง ขอบุญบารมีของพ่อปู่ช่วยปัดเป่าโรคภัยไข้เจ็บให้ออกจากชีวิตของเรา คนในครอบครัวของเรา ซึ่งให้เราท่องตามคาถาที่ตั้งไว้ด้านหน้าองค์ปู่เลยจ้า",
        },
        {
          image: require("~/assets/img/monastery/nakprok/n6.jpg"),
          content: "ความศักดิ์สิทธิ์ของหลวงพ่อเจ้าสัวนี้ ประชาชนเดินทางมากราบไหว้อย่างไม่ขาดสาย โดยเฉพาะการขอพรเรื่องความเจริญรุ่งเรืองในหน้าที่การงาน และการประกอบธุรกิจต่างๆ ซึ่งเขาบอกว่าหลวงพ่อเจ้าสัว จะให้ในเรื่องมีทรัพย์สมบัติ ที่ดิน ธุระกิจ",
        },
        {
          image: require("~/assets/img/monastery/nakprok/n8.jpg"),
          content: "มาวัดนาคปรก สิ่งที่พลาดไม่ได้เลย คือ การเดินลอดอุโบส์ถ ซึ่งจะช่วยไล่คุณไสย มนต์ดำ สิ่งอัปมงคล ทั้งหลายที่ติดมาแต่ชาติก่อน ชาตินี้ จะหลุดไป และยังทำให้เราแคล้วคลาดโรคภัยไข้เจ็บ เสริมความเป็นสิริมงคล ให้กับตัวผู้ที่ได้ลอดโบส์ถเเห่งนี้อีกด้วย",
        },

        {
          image: require("~/assets/img/monastery/nakprok/n10.JPG"),
          content: "วัดเเห่งนี้ ถ้าใครอยากมาทำสังฆทาน หรือ ถวายผ้าไตร ก็สามารถมาทำได้",
        },

        {
          image: require("~/assets/img/monastery/nakprok/n9.jpg"),
          content: "พระพุทธรูปองค์หน้า คือ หลวงพ่อโต องค์หลัง คือ หลวงพ่อใหญ่ วิธีการขอพรจากหลวงโตให้กระซิบที่ข้างหูหลวงพ่อ ผู้ชายกระซิบด้านขวา ผู้หญิงกระซิบด้านซ้าย ผู้ที่มากราบไหว้ จะขอพรในเรื่องของ",
        },
      ],
      photoAll: [
        {
          image: require("~/assets/img/monastery/nakprok/n1.jpg"),
        },
        {
          image: require("~/assets/img/monastery/nakprok/n2.jpg"),
        },
        {
          image: require("~/assets/img/monastery/nakprok/n3.jpg"),
        },
        {
          image: require("~/assets/img/monastery/nakprok/n4.jpg"),
        },
        {
          image: require("~/assets/img/monastery/nakprok/n5.jpg"),
        },
        {
          image: require("~/assets/img/monastery/nakprok/n7.jpg"),
        },

        {
          image: require("~/assets/img/monastery/nakprok/n9.jpg"),
        },
        {
          image: require("~/assets/img/monastery/nakprok/n10.JPG"),
        },
        {
          image: require("~/assets/img/monastery/nakprok/n11.JPG"),
        },
        {
          image: require("~/assets/img/monastery/nakprok/n8.jpg"),
        },
      ]
    }
  }
}
</script>

<style scoped>

.dataSource {
  font-size: 1rem;
  color: #a4a3a3;
}

.dataSource:hover {
  color: #be977a;
}
</style>
