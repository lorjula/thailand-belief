<template>
  <div class="container " style="text-align: center;">

    <div class="" style="padding-top: 6rem;">
      <h2 style="color: #A0826A;">วัดวาอาราม</h2>
      <h5 class="pt-3" style="color: #797979;">
        เชื่อกันว่าหลายๆคนเมื่อมีความทุกข์ สิ่งแรกที่เรานึกถึงนั้นก็คงไม่พ้นการเข้าวัด
        ทำบุญสร้างกุศลเพื่อให้ชีวิตตนพ้นจากความทุกข์เหล่านี้ และนั้นคือสิ่งที่ถูกต้อง
        ซึ่งในประเทศไทยเป็นประเทศที่มี <br>วัดวาอารามมากมาย
        ซึ่งบรรพบุรุษของเราได้สร้างไว้ให้กับคนรุ่นหลังได้เห็นถึงความสวยงามของวัฒนธรรม ขนบธรรมเนียบประเพณี
        เพื่อสร้างคุณงามความดีกันต่อไป</h5>
    </div>
    <nuxt-link to="/monastery/bangkok/nakprong" style="text-decoration: none;">
      <div class="row" style="margin-top: 6rem;margin-bottom: 6rem;text-align: center;">


        <div class="col-md-6 col-sm-6 order-lg-2">
          <div style="background-color: #737D74;">
            <img class="monastery" src="~/assets/img/monastery/nakprok.jpg">
          </div>
        </div>

        <div class="col-md-6 col-sm-6 order-lg-1" style="background-color: white">
          <div style="padding: 4rem;">
            <h6 class="province " style="padding-top: 2rem;">กรุงเทพฯ</h6>
            <h3 class="temple" style="padding-top: 2rem;">วัดนาคปรก</h3>
            <div class="detail">
              <h6 class="history " style="padding-top: 1rem;  font-size: 1.1rem;  line-height: 2rem;">
                สมัยอยุธยาตอนปลาย-กรุงรัตนโกสินทร์ตอนต้น (ร.๓-๔)
                มีพ่อค้าเรือสำเภาชาวจีน ชื่อ เจ้าสัวพุก แซ่ตัน เป็นผู้คิดริเริ่มก่อสร้างวัดขึ้น
                เพื่อใช้เป็นสถานที่ประกอบพิธีกรรม
                และศาสนกิจทางพระพุทธศาสนา</h6>
              <h6 class="history" style="padding-top: 2rem;font-size: 1.1rem;  line-height: 2rem;">
                ได้อัญเชิญพระพุทธรูปปางมารวิชัยมาจากเมืองสุโขทัย
                มาประดิษฐานไว้ในวิหาร ชาวบ้านจึงได้เรียกว่า “วัดนาคปรก”
              </h6>
            </div>
          </div>
        </div>

      </div>
    </nuxt-link>

    <div class="bottom mt-5" style="padding-bottom: 6rem;">
      <nuxt-link to="/monastery/group-monastery">
        <button type="button" class="btn btn-bottom"
                style="padding-left: 50px;padding-right: 50px;">วัดวาอาราม
        </button>
      </nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  name: "monastery"
}
</script>

<style scoped>
.monastery {
  width: 100%;
}

.col-md-6 {
  padding-left: 0px;
  padding-right: 0px;
}

.province, .temple, .history {
  color: #797979;
}

.history {
  text-align: initial;
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

  .monastery {
    padding: 2rem;
  }

  .detail {
    height: 5rem;
    overflow: hidden;
  }
}

/*Galaxys5*/
@media only screen and (min-width: 360px) {
  .pt-3 {
    margin-left: 1rem;
    margin-right: 1rem;
    line-height: 1.6;
  }

  .monastery {
    padding: 2rem;
  }

  .detail {
    height: 5rem;
    overflow: hidden;
  }
}

/*iphone 6/7/8*/
@media only screen and (min-width: 375px) {
  .pt-3 {
    margin-left: 1rem;
    margin-right: 1rem;
    line-height: 1.6;
  }

  .monastery {
    padding: 4rem;
  }

  .detail {
    height: 5rem;
    overflow: hidden;
  }
}

/*I678plus*/
@media only screen and (min-width: 414px) {
  .pt-3 {
    margin-left: 1rem;
    margin-right: 1rem;
    line-height: 1.6;
  }

  .monastery {
    padding: 4rem;
  }

  .detail {
    height: 5rem;
    overflow: hidden;
  }
}

/*surfaceDuo*/
@media only screen and (min-width: 540px) {
  .pt-3 {
    margin-left: 1rem;
    margin-right: 1rem;
    line-height: 1.6;
  }

  .monastery {
    padding: 2rem;
  }

  .detail {
    height: 5rem;
    overflow: hidden;
  }
}

/*ipad*/
@media only screen and (min-width: 768px) {
  .pt-3 {
    margin-left: 2rem;
    margin-right: 2rem;
    line-height: 1.6;
  }

  .monastery {
    padding: 5rem;
  }

  .detail {
    height: 11rem;
    overflow: hidden;
  }
}

/*ipadPro*/
@media only screen and (min-width: 1024px) {
  .pt-3 {
    margin-left: 2rem;
    margin-right: 2rem;
    line-height: 1.6;
  }

  .monastery {
    padding: 5rem;
  }

  .detail {
    height: 11rem;
    overflow: hidden;
  }
}

/*pc*/
@media only screen and (min-width: 1024px) {
  .pt-3 {
    margin-left: 2rem;
    margin-right: 2rem;
    line-height: 1.6;
  }

  .monastery {
    padding: 5rem;
  }

  .detail {
    height: auto;
    overflow: hidden;
  }


}
</style>
