<template>
  <div style="background-color: #f7f6f4;">
    <Navbar/>
    <div class="container">
      <div class="row">
        <div class="col-sm">

          <div class="" style="margin-top: 6rem; text-align: center;">
            <h2 style="color: #A0826A;">ความเชื่อ "โฉลก"</h2>
            <h5 class="pt-3" style="color: #797979;margin-left:9rem;margin-right: 9rem;line-height: 1.6;">
              ผู้คนสมัยก่อนมักมีความเชื่อต่างๆหลากหลาย เรื่องการเลือกให้ถูกโฉลกกับดวงประจำวันเกิดของตน
              จะเป็นสิ่งที่นำโชคลาภ ความมั่งมี สิริมงคลในชีวิตมาให้กับตน ซึ่งคนไทยเองมีความเชื่อเรื่องดวง
              และความเป็นมงคล
              หากจะทำอะไรก็ต้องคิดคำนึงถึงเรื่องความเชื่อ เพื่อความสบายใจ
            </h5>
          </div>

        </div>
      </div>
    </div>
    <div style="margin-bottom: 15rem;">
      <div class="container" style="margin-top: 9rem;">
        <div class="row" style="">
          <div class="col-md-3">
            <nuxt-link to="/belief/auspicious-color">
              <img class="belief" src="~/assets/img/belief/auspiciouscolor/b1.svg">
            </nuxt-link>
          </div>
          <div class="col-md-3">
            <nuxt-link to="/belief/homecolor">
              <img class="belief" src="~/assets/img/belief/homecolor/h1.png">
            </nuxt-link>
          </div>
          <div class="col-md-3">
            <nuxt-link to="/belief/carcolor">
              <img class="belief" src="~/assets/img/belief/carcolor/c1.png">
            </nuxt-link>
          </div>
          <div class="col-md-3">
            <nuxt-link to="/belief/bed">
              <img class="belief" src="~/assets/img/belief/bed-sheet/bedsheet.png">
            </nuxt-link>
          </div>
          <div class="col-md-3">
            <nuxt-link to="/belief/tree">
              <img class="belief" src="~/assets/img/belief/tree/tree.png">
            </nuxt-link>
          </div>
          <div class="col-md-3">
            <nuxt-link to="/belief/phone">
              <img class="belief" src="~/assets/img/belief/phone/phone.png">
            </nuxt-link>
          </div>
          <div class="col-md-3">
            <nuxt-link to="/belief/wallet">
              <img class="belief" src="~/assets/img/belief/wallet/wallet.png">
            </nuxt-link>
          </div>
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
  name: "group-belief",
  components: {Footer, Navbar}
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
</style>
