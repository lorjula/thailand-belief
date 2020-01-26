<template>
  <div>
    <nav class=" navbar navbar-expand-sm navbar-light" id="nav">
      <a class="navbar-brand" href="#">
        <img class="logo" src="~assets/img/logo.svg" alt="Thailand Belef"/>
      </a>
      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarTogglerDemo02"
        aria-controls="navbarTogglerDemo02"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarTogglerDemo02" style="background-color:white;">
        <ul class="navbar-nav">
          <li class="nav-item active">
            <nuxt-link class="nav-link" to="/" style=width:76px;>หน้าหลัก <span class="sr-only">(current)</span>
            </nuxt-link>
          </li>
          <li class="nav-item dropdown">
            <nuxt-link class="nav-link dropdown-toggle" to="#" id="navbarDropdown" role="button" data-toggle="dropdown"
                       aria-haspopup="true" aria-expanded="false">
              ความเชื่อ
            </nuxt-link>
            <div class="dropdown-menu" aria-labelledby="navbarDropdown">
              <nuxt-link class="dropdown-item" to="/auspicious-color">สีมงคลประจำวันเกิด</nuxt-link>
              <nuxt-link class="dropdown-item" to="/sacred-tree">ต้นไม้มงคล</nuxt-link>
              <nuxt-link class="dropdown-item" to="/house-color">สีบ้านฮ่วงจุ้ย</nuxt-link>
              <nuxt-link class="dropdown-item" to="/fountain">น้ำพุเสริมฮวงจุ้ย</nuxt-link>
              <nuxt-link class="dropdown-item" to="/phonecase">สีเคสมือถือประจำวันเกิด</nuxt-link>
              <nuxt-link class="dropdown-item" to="/carcolor">โฉลกสีรถ</nuxt-link>
              <nuxt-link class="dropdown-item" to="#"></nuxt-link>
            </div>
          </li>
        </ul>
        <div class="search">
          <img src="~assets/img/searchon.png" class="img-search">
          <input placeholder="ค้นหา..." class="input-search">
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
  export default {
    name: "navbar"
  }
</script>

<style scoped>


  /* Extra small devices (phones, 600px and down) */
  @media only screen and (max-width: 600px) {
    #nav {
      background-color: white;
      margin-top: 0%;
      height: 80px;
    }


    .logo {
      width: 222px;
      height: 100%;
      padding-left: 0%;
    }

    .navbar-brand {
      padding-left: 7%;
      display: inline-block;
      padding-top: 0.3125rem;
      padding-bottom: 0.3125rem;
      margin-right: 0rem;
      font-size: 1.25rem;
      line-height: inherit;
      white-space: nowrap;
      background-color: white;
    }

    .navbar {
      position: relative;
      display: -webkit-box;
      display: flex;
      flex-wrap: wrap;
      -webkit-box-align: center;
      align-items: center;
      -webkit-box-pack: justify;
      justify-content: space-between;
      padding: 0;
    }

    .navbar-nav {
      padding-left: 26px;
    }

    .nav-item {
    }

    .search {
      width: 200px;
      height: 35px;
      border-radius: 30px;
      border-color: #CECECE;
      border-style: solid;
      border-width: thin;
      margin-bottom: 1%;
      margin-left: 23px;
      border-left-width: 0px;
      padding-left: 0px;
    }

    .img-search {
      height: 71%;
      padding-left: 5%;
      padding-top: 2%;
    }

    .input-search {
      border: 0;
      width: 152px;
      background: none;
      input: unset;
      outline: none;
      padding-top: 1%;
    }
  }


  /* Small devices (portrait tablets and large phones, 600px and up) */
  @media only screen and (min-width: 600px) {
  }


  /* Medium devices (landscape tablets, 768px and up) */
  @media only screen and (min-width: 768px) {
    .search {
      width: 27px;
    }
  }


  /* Large devices (laptops/desktops, 992px and up) */
  @media only screen and (min-width: 992px) {
    #nav {
      background-color: white;
      margin-top: 0%;
      height: 80px;
    }


    .logo {
      width: 90%;
      height: 100%;
      padding-left: 0%;
    }

    .navbar-brand {
      padding-left: 7%;
      display: inline-block;
      padding-top: 0.3125rem;
      padding-bottom: 0.3125rem;
      margin-right: 0rem;
      font-size: 1.25rem;
      line-height: inherit;
      white-space: nowrap;
      background-color: white;
    }

    .navbar {
      position: relative;
      display: -webkit-box;
      display: flex;
      flex-wrap: wrap;
      -webkit-box-align: center;
      align-items: center;
      -webkit-box-pack: justify;
      justify-content: space-between;
      padding: 0;
    }

    .navbar-nav {
      padding-left: 46%;
    }

    .nav-item {
    }

    .search {
      width: 200px;
      height: 35px;
      border-radius: 30px;
      border-color: #CECECE;
      border-style: solid;
      margin-left: 2%;
      border-width: thin;
      margin-bottom: 1%;
    }

    .img-search {
      height: 71%;
      padding-left: 5%;
      padding-top: 2%;
    }

    .input-search {
      border: 0;
      width: 152px;
      background: none;
      input: unset;
      outline: none;
      padding-top: 1%;
    }
  }


  /* Extra large devices (large laptops and desktops, 1200px and up) */
  @media only screen and (min-width: 1200px) {

  }
</style>
