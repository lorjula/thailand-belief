<template>
  <div style="background: #f4f1ea;padding-top: 1rem;">
    <div style="padding-bottom: 9rem;">
      <div class="container" style="margin-top: 5rem;">
        <div style="text-align: center;color: rgb(121 121 121);margin-bottom: 6rem;">
          <h3>เนื้อหาเเนะนำ</h3>
        </div>
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
  </div>
</template>

<script>
export default {
  name: "recommended"
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
