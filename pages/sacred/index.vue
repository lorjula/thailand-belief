<template>
  <div style="background-color: #f7f6f4;">
    <navbar/>
    <div class="container">
      <div class="row">
        <div class="col-sm">

          <div class="" style="margin-top: 6rem; text-align: center;">
            <h2 style="color: #A0826A;">สถานที่ศักดิ์สิทธิ์</h2>
            <h5 class="pt-3" style="color: #797979;">
              ในประเทศไทยเอง มีความเชื่อเรื่องสิ่งที่มองไม่เห็น และมีการปฏิบัติ
              ต่อสิ่งศักดิ์สิทธิ์ท่ีแสดงถึงความเชื่อในสังคมไทยร่วมสมัยด้วยการเคารพบูชาหลายวิธีการ รูปแบบ
              ของส่ิงศักดิ์สิทธ์ิและความเชื่อต่อสิ่งศักดิ์สิทธิ์พบได้ในหลายตำาแหน่งแห่งที่ไม่เว้นแม้แต่ในสถาน
              ศึกษาซึ่งเป็นสถาบันท่ีบรรจุความรู้สมัยใหม่ไว้ ในมหาวิทยาลัยอุบลราชธานีก็เช่นกัน มีการบูชา
              สิ่งศักด์ิสิทธิ์ตามสถานที่ต่างๆ ทั้งในบริเวณอาคารและรอบนอกอาคาร
            </h5>
          </div>

        </div>
      </div>
    </div>
    <div style="margin-bottom: 15rem;">
      <div class="container" style="margin-top: 9rem;">
        <div class="row" style="">
          <template v-for="item in sacred">
            <div class="col-md-3">
              <nuxt-link :to="item.link">
                <img class="belief" :src="item.image">
              </nuxt-link>
            </div>
          </template>

        </div>
      </div>
    </div>
    <Footer/>
  </div>
</template>

<script>
import Navbar from "~/components/nav/navbar";
import Footer from "~/components/footer/footer";

export default {
  name: "indix",
  components: {Footer, Navbar},
  data() {
    return {
      sacred: [
        {
          link: "/sacred/courtprajaotakPhayathai3",
          image: require("~/assets/img/sacred/prajaotak/courtprajaotak-phayathai3.png"),
        },
      ]
    }
  }
}
</script>

<style scoped>

.belief {
  width: 100%;
}

.belief:hover {
  -ms-transform: scale(1.03);
  -webkit-transform: scale(1.03);
  transform: scale(1.03);
}


/*iphone5/se*/
@media only screen and (max-width: 320px) {
  .pt-3 {
    margin-left: 1rem;
    margin-right: 1rem;
    line-height: 1.6;
  }

}

/*Galaxys5*/
@media only screen and (min-width: 360px) {
  .pt-3 {
    margin-left: 1rem;
    margin-right: 1rem;
  }


}

/*iphone 6/7/8*/
@media only screen and (min-width: 375px) {
  .pt-3 {
    margin-left: 1rem;
    margin-right: 1rem;
  }


}

/*I678plus*/
@media only screen and (min-width: 414px) {
  .pt-3 {
    margin-left: 1rem;
    margin-right: 1rem;
  }


}

/*surfaceDuo*/
@media only screen and (min-width: 540px) {
  .pt-3 {
    margin-left: 1rem;
    margin-right: 1rem;
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
