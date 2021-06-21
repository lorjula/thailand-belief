<template>
  <div class="" style="margin-bottom: 6rem;">
    <div class="row" style="margin-top: 6rem;text-align: center;">
      <div class="col-md col-sm" style="background-color: white;">
        <nuxt-link to="">
          <div class="imgFortune">
            <img src="~assets/img/fortune/f1.png" style="width: 100%;">
          </div>
        </nuxt-link>
      </div>
    </div>

    <div class="row">

      <div class="col-md-3 col-sm-3" style="background-color: white">
        <nuxt-link to="">
          <div class="imgFortune" style="">
            <img src="~assets/img/fortune/f2.png" style="width: 100%;">
          </div>
        </nuxt-link>
      </div>
      <div class="col-md-3 col-sm-3" style="background-color: white">
        <nuxt-link to="">
          <div class="imgFortune" style="">
            <img src="~assets/img/fortune/f3.png" style="width: 100%;">
          </div>
        </nuxt-link>
      </div>
      <div class="col-md-3 col-sm-3" style="background-color: white">
        <nuxt-link to="">
          <div class="imgFortune" style="">
            <img src="~assets/img/fortune/f4.png" style="width: 100%;">
          </div>
        </nuxt-link>
      </div>
      <div class="col-md-3 col-sm-3" style="background-color: white">
        <nuxt-link to="">
          <div class="imgFortune" style="">
            <img src="~assets/img/fortune/f5.png" style="width: 100%;">
          </div>
        </nuxt-link>
      </div>


    </div>

  </div>
</template>

<script>
export default {
  name: "fortuneImg"
}
</script>

<style scoped>
.col-md, .col-md-3, .col-sm-3 {
  padding: 0.2rem;
}

.imgFortune:hover {
  -ms-transform: scale(0.9);
  -webkit-transform: scale(0.9);
  transform: scale(0.9);
  background-color: #c9a081;
}
</style>
