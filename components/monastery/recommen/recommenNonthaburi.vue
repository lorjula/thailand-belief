<template>
  <div style="background: #f4f1ea;padding-top: 1rem;">
    <div style="padding-bottom: 15rem;">
      <div class="container" style="margin-top: 5rem;">
        <div style="text-align: center;color: rgb(121 121 121);margin-bottom: 6rem;">
          <h3>เนื้อหาเเนะนำ</h3>
        </div>


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
  </div>

</template>

<script>
export default {
  name: "recommenNonthaburi"
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
</style>
