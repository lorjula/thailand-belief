<template>
  <div class="container " style="text-align: center;">
    <div class="" style="margin-top: 6rem;">
      <h2 style="color: #A0826A;">ความเชื่อ "โฉลก"</h2>
      <h5 class="pt-3" style="color: #797979;">
        ผู้คนสมัยก่อนมักมีความเชื่อต่างๆหลากหลาย เรื่องการเลือกให้ถูกโฉลกกับดวงประจำวันเกิดของตน
        จะเป็นสิ่งที่นำโชคลาภ ความมั่งมี สิริมงคลในชีวิตมาให้กับตน ซึ่งคนไทยเองมีความเชื่อเรื่องดวง และความเป็นมงคล
        หากจะทำอะไรก็ต้องคิดคำนึงถึงเรื่องความเชื่อ เพื่อความสบายใจ
      </h5>
    </div>

    <div class="container-fluid">
      <div class="row" style="margin-top: 6rem;">
        <div class="col-md-4 col-sm-6">
          <nuxt-link to="/belief/auspicious-color">
            <img class="belief" src="~/assets/img/belief/auspiciouscolor/b1.svg">
          </nuxt-link>
        </div>
        <div class="col-md-4 col-sm-6">
          <nuxt-link to="/belief/homecolor">
            <img class="belief" src="~/assets/img/belief/homecolor/h1.png">
          </nuxt-link>
        </div>
        <div class="col-md-4 col-sm-6">
          <nuxt-link to="/belief/carcolor">
            <img class="belief" src="~/assets/img/belief/carcolor/c1.png">
          </nuxt-link>
        </div>
        <div class="col-md-4 col-sm-6">
          <nuxt-link to="/belief/bed">
            <img class="belief" src="~/assets/img/belief/bed-sheet/bedsheet.png">
          </nuxt-link>
        </div>
        <div class="col-md-4 col-sm-6">
          <nuxt-link to="/belief/tree">
            <img class="belief" src="~/assets/img/belief/tree/tree.png">
          </nuxt-link>
        </div>
        <div class="col-md-4 col-sm-6">
          <nuxt-link to="/belief/phone">
            <img class="belief" src="~/assets/img/belief/phone/phone.png">
          </nuxt-link>
        </div>
      </div>

    </div>

    <div class="bottom mt-5" style="padding-bottom: 6rem;">
      <nuxt-link to="/belief/group-belief">
        <button type="button" class="btn btn-bottom btn-outline"
                style="padding-left: 50px;padding-right: 50px;">
          ความเชื่อ
        </button>
      </nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  name: "belief"
}
</script>

<style scoped>
.belief {
  width: 100%;
}

.col-md-4 {
  padding-left: 0px;
  padding-right: 0px;
}

.belief:hover {
  -ms-transform: scale(1.03);
  -webkit-transform: scale(1.03);
  transform: scale(1.03);
}

.btn-bottom {
  width: 14rem;
  background-color: #95a295;
  color: #ffffff;
}

.btn-bottom:hover {
  box-shadow: 0px 0px 6px 1px #99b19e;
  background-color: #626b63;
  color: #ffffff;
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
    line-height: 1.6;
  }
}

/*iphone 6/7/8*/
@media only screen and (min-width: 375px) {
  .pt-3 {
    margin-left: 1rem;
    margin-right: 1rem;
    line-height: 1.6;
  }
}

/*I678plus*/
@media only screen and (min-width: 414px) {
  .pt-3 {
    margin-left: 1rem;
    margin-right: 1rem;
    line-height: 1.6;
  }
}

/*surfaceDuo*/
@media only screen and (min-width: 540px) {
  .pt-3 {
    margin-left: 1rem;
    margin-right: 1rem;
    line-height: 1.6;
  }
}

/*ipad*/
@media only screen and (min-width: 768px) {
  .pt-3 {
    margin-left: 2rem;
    margin-right: 2rem;
    line-height: 1.6;
  }
}

/*ipadPro*/
@media only screen and (min-width: 1024px) {
  .pt-3 {
    margin-left: 2rem;
    margin-right: 2rem;
    line-height: 1.6;
  }
}

/*pc*/
@media only screen and (min-width: 1024px) {
  .pt-3 {
    margin-left: 2rem;
    margin-right: 2rem;
    line-height: 1.6;
  }


}

</style>
