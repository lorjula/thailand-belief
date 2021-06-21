<template>
  <div style="background-color:#F7F6F4;">

    <div style="background-color: #ffffff;">

      <navbar/>

    </div>

    <div class="" style="background-color:#F7F6F4; margin-bottom: 9rem;">
      <div class="container" style="text-align: center;">
        <div class="" style="padding-top: 6rem;">
          <h2 style="color: #A0826A;">ศาลพระเจ้าตากสินมหาราช</h2>
          <h5 class="pt-3" style="color: #797979;margin-left:4rem;margin-right: 4rem;line-height: 1.6;">

          </h5>
        </div>

        <template v-for="item in monastery">
          <div class="row " style="margin-top: 9rem;">
            <div class="col-md-2"></div>
            <div class="col-md-8">
              <img style="object-fit: cover;width:100%;"
                   :src="item.image">
            </div>
            <div class="col-md-2"></div>

          </div>

          <div class="row" style="margin-top: 5rem;">
            <div class="col-md">
              <h5 class="pt-3" style="color: #797979;margin-left:4rem;margin-right: 4rem;line-height: 1.6;">
                {{ item.content }}
              </h5>
            </div>
          </div>
        </template>

        <a class="dataSource" href="https://www.facebook.com/papaiwatofficial/posts/1012538735580201"
           style="text-decoration:none; ">
          <h6 style=" margin-top: 5rem; width: 100%;">
            ขอบคุณข้อมูล:papaiwatofficial</h6>
        </a>

      </div>
    </div>

    <Map :map="map" :day="day"/>

    <RecommendSacred/>

    <Footer/>
  </div>
</template>

<script>
import Navbar from "~/components/nav/navbar";
import Footer from "~/components/footer/footer";
import Map from "~/components/monastery/map";
import RecommenBangkok from "~/components/monastery/recommen/recommenBangkok";
import Recommended from "~/components/belief/recommended";
import RecommendSacred from "~/components/sacred/recommendSacred";

export default {
  name: "index",
  components: {RecommendSacred, Recommended, RecommenBangkok, Map, Footer, Navbar}
  ,
  data() {
    return {
      map: {
        link: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3875.9252021696734!2d100.46188671446345!3d13.722978201658897!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x30e2984634badc79%3A0xd5f0e330080118f4!2sPhyathai%203%20Hospital!5e0!3m2!1sen!2sth!4v1624204418440!5m2!1sen!2sth",
        address: "111 ถ. เพชรเกษม แขวง ปากคลองภาษีเจริญ เขตภาษีเจริญ กรุงเทพมหานคร 10160"
      },
      day: {
        sunday: "24 ชม.",
        monday: "24 ชม.",
        tuesday: "24 ชม.",
        wednesday: "24 ชม.",
        thursday: "24 ชม.",
        friday: "24 ชม.",
        saturday: "24 ชม.",
      },
      monastery: [
        {
          image: require("~/assets/img/sacred/prajaotak/pra3.jpg"),
          content: "ศาลพระเจ้าตากสินมหาราช อยู่หน้าทางเข้า รพ.พญาไท 3 ซึ่งคนที่เข้ามากราบไหว้ขอพร มีทั้งคนที่เดินผ่านหน้าโรงพยาบาล เเละคนที่เข้ามารักษาในโรงพยาบาลแห่งนี้ เรื่อยๆ บางคนมากราบขอพรในเรื่องของหน้าที่การงาน โชคลาภ สุขภาพ ก็สำเร็จกัน นำพวงมลัยหรือรูปปั้นไก่ชนมาเเก้บน "
          ,

        },
        {
          image: require("~/assets/img/sacred/prajaotak/pra2.jpg"),
          content: "คาถาบูชาสมเด็จพระเจ้าตากสินมหาราช",
        },

      ],
      photoAll: [
        {
          image: require("~/assets/img/sacred/prajaotak/s1.jpg"),
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
