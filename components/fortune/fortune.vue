<template>

  <div class="container " style="text-align: center;">
    <div class="" style="padding-top: 6rem;">
      <h2 style="color: #A0826A;">ฮวงจุ้ย</h2>
      <h5 class="pt-3" style="color: #797979;">สีมงคล ตามวันเกิด
        เสริมมงคลแต่ละด้านให้ดี และ สีกาลกิณี ที่ควรเลี่ยง สีมงคล ตามวันเกิด เสริมมงคลแต่ละด้านให้ดี</h5>
    </div>

    <FortuneImg/>

    <div class="bottom mt-5" style="padding-bottom: 6rem;">
      <button type="button" class="btn btn-bottom"
              style="padding-left: 50px;padding-right: 50px;">ฮวงจุ้ย
      </button>
    </div>
  </div>
</template>

<script>
import FortuneImg from "~/components/fortune/fortuneImg";

export default {
  name: "fortune",
  components: {FortuneImg}
}
</script>

<style scoped>

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
