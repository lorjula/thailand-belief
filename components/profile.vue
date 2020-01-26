<template>
  <div>
    <div class="border-top">
      <div class="margin-left">
        <div class="media">
          <img src="~assets/img/warunrada.jpg" class="mr-3">
          <div class="media-body">
            <h5 class="mt-0">LORJULA_DESIGN</h5>
            <h6 class="mt-01">นักออกแบบเว็บไซต์ โลโก้ การ์ตูน ภาพเสมือน เขียนบทความ Thailand
              belief,samoonpai,lorjula_Design</h6>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

  export default {
    name: "profile"
  }
</script>

<style scoped>
  /* Extra small devices (phones, 600px and down) */
  @media only screen and (max-width: 600px) {
    .border-top {
      margin-top:0px;
      border-color: rgb(47, 43, 99);
    }

    .margin-left {
      margin-left: 0px;
      padding-right: 40px;
      margin-top: 0px;
    }

    .media {
      margin-left: 28px;
      padding-top: 37px;
      width: 352px;
    }

    .mr-3 {
      width: 75px;
      height: 75px;
      border-radius: 100%;
    }

    .mt-0 {
      font-size: 1rem;
    }

    .mt-01 {
      font-size: 0.9rem;
    }
  }

  /* Small devices (portrait tablets and large phones, 600px and up) */
  @media only screen and (min-width: 600px) {
  }


  /* Medium devices (landscape tablets, 768px and up) */
  @media only screen and (min-width: 768px) {
  }


  /* Large devices (laptops/desktops, 992px and up) */
  @media only screen and (min-width: 992px) {
    .border-top {
      margin-top:30px;
      border-color: #2f2b63
    }

    .margin-left {
      margin-left: 39px;
      padding-right: 40px;
    }

    .media {
      padding-top: 37px;
      width: 865px;
      margin-left: 85px;
      margin-bottom: 25px;
    }

    .mr-3 {
      width: 120px;
      height: 120px;
      border-radius: 100%;
    }

    .media-body {

    }

    .mt-0 {
    }
  }


  /* Extra large devices (large laptops and desktops, 1200px and up) */
  @media only screen and (min-width: 1200px) {

  }
</style>
