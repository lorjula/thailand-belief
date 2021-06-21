<template>
  <div style="background-color:#F7F6F4;">

    <div style="background-color: #ffffff;">

      <Navbar/>

    </div>

    <div class="" style="background-color:#F7F6F4; margin-bottom: 9rem;">
      <div class="container" style="text-align: center;">
        <div class="" style="padding-top: 6rem;">
          <h2 style="color: #A0826A;">วัดแดงธรรมชาติ</h2>
          <h5 class="pt-3" style="color: #797979;margin-left:4rem;margin-right: 4rem;line-height: 1.6;">
            ในปี พ.ศ.2400 ชื่อของวัดนั้นสันนิษฐานว่า มีชาวบ้านนำวัวแดงมาเลี้ยงใน
            บริเวณวัด โดยท่านเจ้าอาวาสยังได้จัดตั้งพิพิธภัณฑ์พื้นบ้านหรือศูนย์อนุรักษ์และฟื้นฟูศิลปวัฒนธรรมบ้านวัดแดง
            ซึ่งเป็นที่รวบรวมของใช้
            เก่าแก่เพื่อให้เป็นที่ศึกษารุ่นหลังต่อไป ภายในบริเวณวัดมีศาสนสถาน
            และปูชนียวัตถุที่สำคัญควรค่าแก่การอนุรักษ์ และศึกษาในด้านของ สถาปัตยกรรม ศิลปกรรม จิตรกรรม ต่างๆ อย่างมากมาย

          </h5>
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
          <h6 style=" margin-top: 5rem; width: 100%;"></h6>
        </a>

      </div>
    </div>


    <Map :map="map" :day="day"/>

    <RecommenNonthaburi/>

    <Footer/>
  </div>
</template>

<script>
import Footer from "~/components/footer/footer";
import Navbar from "~/components/nav/navbar";
import Map from "~/components/monastery/map";
import RecommenNonthaburi from "~/components/monastery/recommen/recommenNonthaburi";

export default {
  name: "dangtumachat",
  components: {RecommenNonthaburi, Map, Navbar, Footer}
  ,
  data() {
    return {
      map: {
        link: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3873.2054505221345!2d100.47996981446485!3d13.886660197896276!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x30e28527cbd63935%3A0x5b4e0cb7e36aa4d4!2sWat%20Daeng%20Thammachat!5e0!3m2!1sen!2sth!4v1624198780307!5m2!1sen!2sth",
        address: "73/46 1, บางรักน้อย 5 ตำบล ไทรม้า อำเภอเมืองนนทบุรี นนทบุรี 11000"
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
          image: require("~/assets/img/monastery/dangtumachat/dan1.jpg"),
          content: "พระปรางนาคปรก ริมแม่น้ำเจ้าพระยา เป็นองค์พระขนาด หน้าตัก 36 ศอก สูง 45 เมตร องค์สีขาวมุก เม็ดพระศกสีดำ พญานาคปรกสีเขียว บริเวณฐานองค์พระนาคปรกด้านล่างมีเศียรพญามุจจลินทร์ขนาดเท่ากับเศียรด้านบน"
          ,
        },
        {
          image: require("~/assets/img/monastery/dangtumachat/dan12.jpg"),
          content: "ภายในพระวิหาร มีหลวงพ่อโต เป็นพระประธาน มีอายุ ประมาณ 300 กว่าปี เป็นพระพุทธรูปที่ใหญ่ที่สุดในจังหวัด นนทบุรี"
          ,
        },
        {
          image: require("~/assets/img/monastery/dangtumachat/dan14.jpg"),
          content: "หลวงพ่อเสือ เป็นพระพุทธรูปปางนาคปรก เนื้อศิลาแลง ด้วยลักษณะของพระพักตร์ที่ดุดันเหมือนเสือ ชาวบ้านจึงเรียกว่า หลวงพ่อเสือ คนที่มาเเก้บน ที่ประสพความสำเร็จ ก็จะเเก้บนด้วยการถวายรูปปั้นเสือ" +
            " เครื่องยืนยันในความศักดิ์สิทธิ์ คือ เมื่อใครอธิฐานได้ดังที่ขอก็จะเเก้บนด้วยการปิดทองพระพุทธรูป ทำให้วัดแห่งนี้มีพระพุทธรูปเหลืองอร่ามด้วยทองทุกองค์"
          ,
        },

      ],
      photoAll: [
        {
          image: require("~/assets/img/monastery/dangtumachat/dan1.jpg"),
        },
        {
          image: require("~/assets/img/monastery/dangtumachat/dan2.jpg"),
        },
        {
          image: require("~/assets/img/monastery/dangtumachat/dan3.jpg"),
        },
        {
          image: require("~/assets/img/monastery/dangtumachat/dan4.jpg"),
        },
        {
          image: require("~/assets/img/monastery/dangtumachat/dan13.jpg"),
        },
        {
          image: require("~/assets/img/monastery/dangtumachat/dan6.jpg"),
        },

        {
          image: require("~/assets/img/monastery/dangtumachat/dan14.jpg"),
        },

        {
          image: require("~/assets/img/monastery/dangtumachat/dan9.jpg"),
        },
        {
          image: require("~/assets/img/monastery/dangtumachat/dan8.jpg"),
        },
        {
          image: require("~/assets/img/monastery/dangtumachat/dan10.jpg"),
        },
        {
          image: require("~/assets/img/monastery/dangtumachat/dan11.jpg"),
        },
        {
          image: require("~/assets/img/monastery/dangtumachat/dan12.jpg"),
        },
        {
          image: require("~/assets/img/monastery/dangtumachat/dan5.jpg"),
        },
        {
          image: require("~/assets/img/monastery/dangtumachat/dan7.jpg"),
        },
      ]
    }
  }
}
</script>

<style scoped>

</style>
