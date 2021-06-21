<template>
  <div class="container mt-3">
    <div>
      <img class="imgCover" src="~/assets/img/cover.png" style="width: 100%;border-radius: 4px;">
    </div>
  </div>
</template>

<script>
export default {
  name: "cover"
}
</script>

<style scoped>

/*iphone5/se*/
@media only screen and (max-width: 320px) {
.imgCover{
  display: none;
}
}

/*Galaxys5*/
@media only screen and (min-width: 360px) {
  .imgCover{
    display: none;
  }
}

/*iphone 6/7/8*/
@media only screen and (min-width: 375px) {
  .imgCover{
    display: none;
  }
}

/*I678plus*/
@media only screen and (min-width: 414px) {
  .imgCover{
    display: none;
  }
}

/*surfaceDuo*/
@media only screen and (min-width: 540px) {
  .imgCover{
    display: none;
  }
}

/*ipad*/
@media only screen and (min-width: 768px) {
  .imgCover{
    display: block;
  }
}

/*ipadPro*/
@media only screen and (min-width: 1024px) {

}

/*pc*/
@media only screen and (min-width: 1024px) {

}
</style>
