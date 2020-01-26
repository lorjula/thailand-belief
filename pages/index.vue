<template>
  <div>

    <Navbar/>

    <nav class="navnav">
      <div class="head">
        <div>
          <div class="Textbox">
            <h6 class="Name-person">Lojula Design</h6>
            <h1 class="Highlight">สีมงคล ตามวันเกิด
              เสริมมงคลแต่ละด้านให้ดี
              และ สีกาลกิณี ที่ควรเลี่ยง</h1>
            <div class="box-Readmore" style="margin-top: 28px;margin-right: 78px;margin-left: 0px;">
              <nuxt-link class="nuxt-link" to="/auspicious-color"><h6 class="btn-btn">อ่านบทความ</h6></nuxt-link>
            </div>
          </div>
        </div>

        <div class="space">
          <img class="headimage" src="~assets/img/colorBirthday.jpg" style="position: absolute;top: 108px;">
          <nuxt-link to="/auspicious-color">
            <div class="texthead-d">
              <img class="search-purple" src="~assets/img/search.png"
                   style="width: 50px;position: absolute;left: 413px;top: 18px;">
              <div class="boxsearch">
                <div class="box" style="border-color: orangered;width:480px">
                  <h1 class="text1" style=" margin-bottom: 0px;padding-top: 9px;padding-right: 64px;color: #F24541;">
                    สีมงคล
                    กาลกีณี</h1>
                </div>
              </div>
              <h1 class="text3" style="margin-top: 20px;">เลือกให้ถูกโฉลก สีวันเกิดเสริมโชคลาค</h1>
            </div>
          </nuxt-link>
        </div>
      </div>
    </nav>

    <div class="row" id="article">
      <div class="col-md-4"></div>
      <div class="col-md-4">บทความล่าสุด</div>
      <div class="col-md-4"></div>
    </div>
    <br/>

    <Article/>
    <Profile/>

  </div>
</template>

<script>

  import Navbar from '../components/navbar';
  import Article from '../components/article';
  import Profile from '../components/profile';

  export default {
    name: "index",
    components: {
      Navbar,
      Article,
      Profile,
    }
  };

</script>

<style>

  .navnav {
    height: 330px;
    background: linear-gradient(90deg, #FCFAFA 50%, #302B63 50%);
  }

  .box-Readmore {
    width: 110px;
    height: 30px;
    border-radius: 19px;
    border-color: rgb(189, 33, 92);
    border-style: solid;
    margin-left: 16%;
    border-width: thin;
    margin-bottom: 3%;
  }

  .btn-btn {
    color: #bd215c;
    text-align: center;
    padding-top: 4%;
  }


  #article {
    padding-top: 2%;
    align-content: center;
    mso-ansi-font-size: medium;
    font-size: 30px;
    text-align: center;
  }

  /*.content {*/
  /*}*/

  /*.blue {*/
  /*  background: #302B63;*/
  /*}*/

  /*.orange {*/
  /*}*/

  /*.carda {*/
  /*  width: 100%;*/
  /*  position: absolute;*/
  /*}*/

  /*.cardx {*/
  /*  width: auto;*/
  /*  margin-top: 2rem;*/
  /*  position: absolute;*/
  /*}*/

  /*.my-card {*/
  /*  margin-left: 2rem;*/
  /*  height: 20rem;*/
  /*  width: 100%;*/
  /*}*/


  .texthead-d:hover {
    -ms-transform: scale(1.1);
    -webkit-transform: scale(1.1);
    transform: scale(1.1);
  }

  .nuxt-link {
    text-decoration: inherit;
  }

  /* Extra small devices (phones, 600px and down) */
  @media only screen and (max-width: 600px) {
    .navnav {
      height: 215px;
    }

    .space {
      height: 1.5rem;
    }

    .Name-person {
      font-size: 0.6rem;
    }

    .Textbox {
      padding-left: 25px;
      width: 157px;
      padding-left: 25px;
      padding-top: 35px;
    }

    .Highlight {
      font-size: 0.9rem;
    }

    .search-purple {
      width: 44px;
      position: absolute;
      left: 298px;
      top: 121px;
      right: 0px;
      display: none;
    }

    .boxsearch {
      background-color: rgb(255, 255, 255);
      height: 42px;
      border-radius: 11px;
      border-color: rgb(206, 206, 206);
      border-style: solid;
      border-width: thin;
      width: 176px;
      position: absolute;
      bottom: 0px;
      top: 122px;
      left: 175px;
    }

    .box-Readmore {

    }

    .headimage {
      position: absolute;
      top: 104px;
      left: 166px;
      border-radius: 9px;
      width: 195px;
    }

    .texthead-d {
      height: 114px;
      margin-left: 0px;
      margin-right: 0px;
      top: 140px;
      left: 0px;
      right: 0px;
      bottom: 0px;
    }

    .text1 {
      font-size: 1.4rem;
      margin-bottom: 0px;
      padding-left: 9px;
      padding-top: 9px;
      padding-right: 0px;
      color: rgb(242, 69, 65);
      width: 239px;
      margin-right: 0px;
      margin-left: 0px;
    }

    .text2 {
      font-size: 1.7rem;
    }

    .text3 {
      color: #ffffff;
      margin-top: 0px;
      margin-bottom: 0px;
      position: absolute;
      top: 156px;
      bottom: 0px;
      right: 0px;
      left: 174px;
      height: 99px;
      width: 186px;
      font-size: 0.7rem;
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

    .navnav {
      height: 390px;
    }

    .Textbox {
      width: 490px;
      padding-left: 107px;
      padding-top: 35px;
    }

    .space {
      height: 2.7rem;
    }

    .headimage {
      width: 561px;
      /*margin-top: 43px;*/
      margin-left: 573px;
      border-radius: 22px;
    }

    .boxsearch {
      background-color: #ffffff;
      height: 88px;
      border-radius: 20px;
      border-color: #CECECE;
      border-style: solid;
      border-width: thin;
    }

    .texthead-d {
      margin-left: 611px;
      margin-right: 0px;
      margin-top: 0px;
      padding-top: 0px;
      margin-bottom: 0px;
      padding-bottom: 0px;
      position: absolute;
      text-align: center;
      top: 184px;
      color: white;
    }

    .text1 {
      font-size: 3.5rem
    }

    .text2 {
      font-size: 2.9rem
    }

    .text3 {
      font-size: 1.9rem
    }
  }

  /* Extra large devices (large laptops and desktops, 1200px and up) */
  @media only screen and (min-width: 1200px) {

  }
</style>
