<template>
  <div>
    <div class="container" id="card">
      <div class="row">
        <div class="col-md-4">
          <nuxt-link class="nuxt-link" to="/auspicious-color">
            <div class="card">
              <img src="~assets/img/colorBirthday.jpg" class="card-img-top"/>
              <div class="text">
                <h1 class="p1">สีมงคล กาลกีณี</h1>
                <h1 class="p2">ประจำวันเกิด</h1>
                <h1 class="p3">เลือกให้ถูกโฉลก สีวันเกิดเสริมโชคลาค</h1>
              </div>
              <div class="card-body">
                <p class="card-text">
                  สีมงคล ตามวันเกิด เสริมมงคล
                  แต่ละด้านให้ดี และ สีกาลกิณี
                  ที่ควรเลี่ยง
                </p>
              </div>
            </div>
          </nuxt-link>
        </div>

        <div class="col-md-4">
          <nuxt-link class="nuxt-link" to="/sacred-tree">
            <div class="card">
              <img src="~assets/img/tree.jpg" class="card-img-top"/>
              <div class="text">
                <h1 class="p1">ต้นไม้มงคล</h1>
                <h1 class="p2">ประจำวันเกิด</h1>
                <h1 class="p3">ต้นไม้เสริม ด้านงาน เงิน ความรัก สุขภาพ</h1>
              </div>
              <div class="card-body">
                <p class="card-text"
                >ต้นไม้ ทำให้เราสบายทางด้านร่างกาย
                  เเล้วเเต่ถ้าเราเลือกให้ถูกโฉลกวันเกิด
                  ก็จะเกิดความมงคลให้กับชีวิตได้</p>
              </div>
            </div>
          </nuxt-link>
        </div>

        <div class="col-md-4">
          <nuxt-link class="nuxt-link" to="/house-color">
            <div class="card">
              <img src="~assets/img/home.jpg" class="card-img-top"/>
              <div class="text">
                <h1 class="p1">สีบ้าน...สร้างสมดุล</h1>
                <h1 class="p2">ตามหลัก ฮวงจุ้ย!</h1>
                <h1 class="p3">สีทาบ้าน ให้ถูกโฉลกกับเจ้าของบ้าน</h1>
              </div>
              <div class="card-body">
                <p class="card-text"
                >สีทาบ้านกับฮวงจุ้ยบ้าน ส่งเสริมในเรื่องของหน้าที่การงาน และการเงิน ทำให้อยู่แล้วเจริญก้าวหน้ายิ่งๆ
                  ขึ้นไป</p>
              </div>
            </div>
          </nuxt-link>
        </div>

      </div>
    </div>

    <div class="container" id="card">
      <div class="row">
        <div class="col-md-4">
          <nuxt-link class="nuxt-link" to="/fountain">
            <div class="card">
              <img src="~assets/img/fountain.svg" class="card-img-top"/>
              <div class="text">
                <h1 class="p1">น้ำพุ</h1>
                <h1 class="p2">เสริมฮวงจุ้ย</h1>
                <h1 class="p3">รูปทาง ว่างทิศไหนเสริมมงคล</h1>
              </div>
              <div class="card-body">
                <p class="card-text">
                  การตกแต่งบ้านต้องคำนึงถึงน้ำพุและบ่อน้ำ เพราะเป็นสิ่งที่ช่วยเสริมเรื่องโชคลาภเงินทองให้กับคนในบ้าน
                </p>
              </div>
            </div>
          </nuxt-link>
        </div>

        <div class="col-md-4">
          <nuxt-link class="nuxt-link" to="/phonecase">
            <div class="card">
              <img src="~assets/img/phonecase.svg" class="card-img-top"/>
              <div class="text">
                <h1 class="p1">สีเคสมือถือ</h1>
                <h1 class="p2">ประจำวันเกิด</h1>
                <h1 class="p3">เลือกเคสมือถือ ยังไงให้รุ่งให้ปังๆๆ</h1>
              </div>
              <div class="card-body">
                <p class="card-text"
                >การเลือกสีเคสให้ถูกกับวันเกิดของเรานั้นจะช่วยในเรื่องของความเสริมสิริมงคล เสริมเรื่องการเงิน, การงาน,
                  เรื่องความรัก</p>
              </div>
            </div>
          </nuxt-link>
        </div>

        <div class="col-md-4">
          <nuxt-link class="nuxt-link" to="/carcolor">
            <div class="card">
              <img src="~assets/img/car.svg" class="card-img-top"/>
              <div class="text">
                <h1 class="p1">โฉลกสีรถ</h1>
                <h1 class="p2">ประจำวันเกิด</h1>
                <h1 class="p3">สีไหนเฮง เสริมสิริมงคล สีไหนห้ามใช</h1>
              </div>
              <div class="card-body">
                <p class="card-text"
                >สีรถถูกโฉลกประจําวันเกิดของแต่ละวันสีไหนเฮง สีรถถูกโฉลกเสริมสิริมงคล หรือ ไม่ควรออกรถสีอะไร</p>
              </div>
            </div>
          </nuxt-link>
        </div>

      </div>
    </div>


  </div>
</template>

<script>
  export default {
    name: "article"
  }
</script>

<style scoped>


  .container {
    background-color: white;
    width: 110%;
  }

  #card {
    align-content: center;
  }

  .card-img-top {
    border-radius: 7px;
  }

  .card {
    width: 22rem;
    height: 20rem;
    border: 0;
  }

  .text {
    position: absolute;
    /*z-index: 999;*/
    margin: 0 auto;
    left: 0;
    right: 0;
    text-align: center;
    top: 14%;
    color: white;
  }

  .p1 {
    font-size: 33px;
  }

  .p2 {
    font-size: 25px;
  }

  .p3 {
    font-size: 15px;
  }

  .p1 .p2 .p3 {
    text-align: center;
    font-weight: bold;
    margin-bottom: 15rem;
  }

  .col-md-4:hover {
    -ms-transform: scale(1.1);
    -webkit-transform: scale(1.1);
    transform: scale(1.1);
  }

  .card-text {
    color: #333333;
    font-size: 1.2rem;
  }

  .nuxt-link {
    text-decoration: inherit;
  }

</style>
