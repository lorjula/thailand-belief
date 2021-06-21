<template>
  <div class="container " style="text-align: center;">
    <div class="" style="padding-top: 6rem;">
      <h2 style="color: #ffffff;">สถานที่ศักดิ์สิทธิ์</h2>
      <h5 class="pt-3" style="color: #ffffff;">
        ในประเทศไทยเอง มีความเชื่อเรื่องสิ่งที่มองไม่เห็น และมีการปฏิบัติ
        ต่อสิ่งศักดิ์สิทธิ์ท่ีแสดงถึงความเชื่อในสังคมไทยร่วมสมัยด้วยการเคารพบูชาหลายวิธีการ รูปแบบ
        ของส่ิงศักดิ์สิทธ์ิและความเชื่อต่อสิ่งศักดิ์สิทธิ์พบได้ในหลายตำาแหน่งแห่งที่ไม่เว้นแม้แต่ในสถาน
        ศึกษาซึ่งเป็นสถาบันท่ีบรรจุความรู้สมัยใหม่ไว้ ในมหาวิทยาลัยอุบลราชธานีก็เช่นกัน มีการบูชา
        สิ่งศักด์ิสิทธิ์ตามสถานที่ต่างๆ ทั้งในบริเวณอาคารและรอบนอกอาคาร
      </h5>
    </div>

    <nuxt-link to="/sacred/courtprajaotakphayathai3" style="text-decoration: none;">
      <div class="row"
           style="text-align: center;background-color: white;">


        <div class="col-md-9" style="">
          <div style="">
            <img class="monastery" src="~/assets/img/sacred/prajaotak/s1.jpg" style="padding: 0rem;width: 100%;">
          </div>
        </div>
        <div class="col-md-3" style="background-color:#F7F6F4;">
          <div style="padding: 0rem;">
            <h3 class="temple" style="padding-top: 2rem; color: #797979;">ศาลพระเจ้าตากสิน</h3>
            <h5 class="history" style="padding-top: 1rem; color: #797979;">สุขภาพ โชคลาภ หน้าที่การงาน</h5>
          </div>
        </div>

      </div>

    </nuxt-link>

    <div class="bottom mt-5" style="padding-bottom: 6rem;">
      <nuxt-link to="/sacred">
        <button type="button" class="btn btn-bottom"
                style="padding-left: 50px;padding-right: 50px;">สถานที่ศักดิ์สิทธิ์
        </button>
      </nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  name: "sacred"
}
</script>

<style scoped>
.monastery {
  width: 100%;
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

  .row {
    margin: 0rem;
    padding: 0.5rem;
  }

  .col-md-9 {
    padding-left: 0rem;
    padding-right: 0px;
  }
}

/*Galaxys5*/
@media only screen and (min-width: 360px) {
  .pt-3 {
    margin-left: 1rem;
    margin-right: 1rem;
    line-height: 1.6;
  }

  .row {
    margin: 1rem;
    padding: 0.5rem;
  }

  .col-md-9 {
    padding-left: 0rem;
    padding-right: 0px;
  }
}

/*iphone 6/7/8*/
@media only screen and (min-width: 375px) {
  .pt-3 {
    margin-left: 1rem;
    margin-right: 1rem;
    line-height: 1.6;
  }

  .row {
    margin: 1rem;
    padding: 0.5rem;
  }

  .col-md-9 {
    padding-left: 0rem;
    padding-right: 0px;
  }
}

/*I678plus*/
@media only screen and (min-width: 414px) {
  .pt-3 {
    margin-left: 1rem;
    margin-right: 1rem;
    line-height: 1.6;
  }

  .row {
    margin: 1rem;
    padding: 0.5rem;
  }

  .col-md-9 {
    padding-left: 0rem;
    padding-right: 0px;
  }
}

/*surfaceDuo*/
@media only screen and (min-width: 540px) {
  .pt-3 {
    margin-left: 1rem;
    margin-right: 1rem;
    line-height: 1.6;
  }

  .row {
    margin: 1rem;
    padding: 0.5rem;
  }

  .col-md-9 {
    padding-left: 0rem;
    padding-right: 0px;
  }
}

/*ipad*/
@media only screen and (min-width: 768px) {
  .pt-3 {
    margin-left: 2rem;
    margin-right: 2rem;
    line-height: 1.6;
  }

  .row {
    margin-top: 6rem;
    margin-bottom: 6rem;
    padding: 0.5rem;
  }

  .col-md-9 {
    padding-left: 0.5rem;
    padding-right: 0px;
  }
}

/*ipadPro*/
@media only screen and (min-width: 1024px) {
  .pt-3 {
    margin-left: 2rem;
    margin-right: 2rem;
    line-height: 1.6;
  }

  .row {
    margin-top: 6rem;
    margin-bottom: 6rem;
    padding: 0.5rem;
  }

  .col-md-9 {
    padding-left: 0.5rem;
    padding-right: 0px;
  }
}

/*pc*/
@media only screen and (min-width: 1024px) {
  .pt-3 {
    margin-left: 2rem;
    margin-right: 2rem;
    line-height: 1.6;
  }

  .row {
    margin-top: 6rem;
    margin-bottom: 6rem;
    padding: 0.5rem;
  }

  .col-md-9 {
    padding-left: 0.5rem;
    padding-right: 0px;
  }


}
</style>
