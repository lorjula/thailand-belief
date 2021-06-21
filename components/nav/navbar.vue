<template>
  <div style="background-color: #F4F1EA; ">
    <div class="container">
      <nav class="navbar navbar-expand-lg pt-3 pb-3" style="padding-left: 0px;padding-right: 0px;}">
        <div class="container" style="padding-left: 0px;padding-right: 0px;">
          <nuxt-link class="navbar-brand" to="/" style="background: no-repeat;">
            <img class="logo" src="~assets/logo/logo.svg" alt="">
          </nuxt-link>

          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
                  aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
            <ul class="nav justify-content-end">
              <li class="nav-item" style="color: #333333;">
                <a class="nav-link active" aria-current="page" href="#">หน้าหลัก</a>
              </li>

              <li class="nav-item dropdown">
                <a class="nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink" role="button"
                   data-bs-toggle="dropdown" aria-expanded="false">
                  ความเชื่อ
                </a>
                <ul class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink"
                    style="background-color:#f4f1ea;color: #3b8070;padding-top: 0px;padding-bottom: 0px;box-shadow: 2px 2px 2px;color: rgb(58 55 55 / 22%);">
                  <li><a class="dropdown-item menuBelief" href="/belief/auspicious-color">สีมงคลประจำวันเกิด</a></li>
                  <li><a class="dropdown-item menuBelief" href="/belief/homecolor">สีบ้านประจำวันเกิด </a></li>
                  <li><a class="dropdown-item menuBelief" href="/belief/carcolor">สีรถประจําวันเกิด</a></li>
                  <li><a class="dropdown-item menuBelief" href="/belief/bed">สีที่นอนประจำวันเกิด </a></li>
                  <li><a class="dropdown-item menuBelief" href="/belief/tree">ต้นไม้มงคลประจำวันเกิด</a></li>
                  <li><a class="dropdown-item menuBelief" href="/belief/phone">สีเคสมือถือประจำวันเกิด</a></li>
                  <li><a class="dropdown-item menuBelief" href="/belief/wallet">สีกระเป๋าตังประจำวันเกิด</a></li>
                </ul>
              </li>

              <li class="nav-item dropdown">
                <a class="nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink" role="button"
                   data-bs-toggle="dropdown" aria-expanded="false">
                  วัดวาอาราม
                </a>
                <ul class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink"
                    style="background-color:#f4f1ea;color: #3b8070;padding-top: 0px;padding-bottom: 0px;box-shadow: 2px 2px 2px;color: rgb(58 55 55 / 22%);">
                  <li>
                    <nuxt-link class="dropdown-item menuBelief" to="/monastery/bangkok/bangkok-group">กรุงเทพฯ
                    </nuxt-link>
                  </li>
                  <li>
                    <nuxt-link class="dropdown-item menuBelief" to="/monastery/nonthaburi/non-group">นนทบุรี</nuxt-link>
                  </li>
                  <li><a class="dropdown-item menuBelief" href="#">อยุธยา</a></li>
                  <li><a class="dropdown-item menuBelief" href="#">สมุทรสาคร</a></li>
                  <li><a class="dropdown-item menuBelief" href="#">ปราจีน</a></li>
                  <li><a class="dropdown-item menuBelief" href="#">สุโขทัย</a></li>
                  <li><a class="dropdown-item menuBelief" href="#">สุรินทร์</a></li>
                </ul>
              </li>

              <li class="nav-item">
                <nuxt-link class="nav-link" to="/sacred" style="padding-right: 0px;">สถานที่ศักดิ์สิทธ์</nuxt-link>
              </li>

              <li class="nav-item dropdown">
                <a class="nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink" role="button"
                   data-bs-toggle="dropdown" aria-expanded="false">
                  ฮวงจุ้ย
                </a>
                <ul class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink"
                    style="background-color:#f4f1ea;color: #3b8070;padding-top: 0px;padding-bottom: 0px;box-shadow: 2px 2px 2px;color: rgb(58 55 55 / 22%);">
                  <li><a class="dropdown-item menuBelief" href="#">น้ำพุเสริมฮ่วงจุ้ย</a></li>
                </ul>
              </li>
            </ul>
          </div>
        </div>
      </nav>
    </div>
  </div>
</template>

<script>
export default {
  name: "navbar",
  header() {
    return {}
  },
  mounted() {

  }
}
</script>

<style scoped>
.navbar-brand {
  padding-left: none;
}

.logo {
  width: 40%;
}

.nav-link {
  color: #797979;
}

.nav-link:hover {
  color: #c9a081;
  font-weight: 500;
}

.dropdown-toggle::after {
  display: none;
}

.dropdown-menu {
  background:;
  color: rgb(59, 128, 112);
  border: none;
}

.menuBelief {
  color: #737d75;
  background-color:;
}

.menuBelief:hover {
  color: #f4f1ea;
  background-color: #c9a081;
}

</style>
