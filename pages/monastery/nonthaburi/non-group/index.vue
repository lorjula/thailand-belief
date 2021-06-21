<template>
  <div style="background-color: #f7f6f4;">
    <Navbar/>
    <div class="container">
      <div class="row">
        <div class="col-sm">

          <div class="" style="margin-top: 6rem; text-align: center;">
            <h2 style="color: #A0826A;">วัดใน "นนทบุรี"</h2>
            <h5 class="pt-3" style="color: #797979;">
              เชื่อกันว่าหลายๆคนเมื่อมีความทุกข์ สิ่งแรกที่เรานึกถึงนั้นก็คงไม่พ้นการเข้าวัด
              ทำบุญสร้างกุศลเพื่อให้ชีวิตตนพ้นจากความทุกข์เหล่านี้ และนั้นคือสิ่งที่ถูกต้อง
              ซึ่งในประเทศไทยเองเป็นประเทศที่มี
              วัดวาอารามมากมาย ซึ่งบรรพบุรุษของเราได้สร้างไว้ให้กับคนรุ่นหลังได้เห็นถึงความสวยงามของวัฒนธรรม
              ขนบธรรมเนียบประเพณี เพื่อสร้างคุณงามความดีกันต่อไป
            </h5>
          </div>

        </div>
      </div>
    </div>
    <div style="margin-bottom: 15rem;">
      <div class="container" style="margin-top: 9rem;">
        <div class="row" style="">
          <template v-for="item in monasteryBangkok">
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
  name: "index",
  components: {Footer, Navbar}
  ,
  data() {
    return {
      monasteryBangkok: [
        {
          link: "/monastery/nonthaburi/non-group/dangtumachat",
          image: require("~/assets/img/monastery/dangtumachat/dangtumachat.png"),
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
