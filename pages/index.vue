<template>
  <div class="container">
    <!--导航-->
    <header-nav></header-nav>

    <!--背景-->
    <bg-body></bg-body>

    <section class="main">
      <div class="content">
        <h1>互联网解决方案机构</h1>
        <h6>我们将创新型的用户体验和独特的设计美学融入到互联网产品中，为您提供有价值的产品解决方案</h6>
      </div>

      <!--锚点链接-->
      <div id="down2">
        <canvas id="downCanvas2" width="50" height="50">你的浏览器不支持canvas，请下载更新版本的浏览器
        </canvas>
      </div>

      <img class="main_img" src="http://oy158wtwk.bkt.clouddn.com/illus-produits.png"/>
    </section>

    <!--我们的项目范围-->
    <section class="home">
      <!--全局曲线-->
      <svg x="0px" y="0px" width="1596.2px" height="2945px" viewBox="0 0 1596.2 2945" class="line">
        <polyline
          points="0.8,0.7 447.5,72.2 537.2,439 946.9,439.8 1595.5,736.4 1148.7,808.2 1059,1175 649.3,1175.8 0.8,1472.4 447.5,1544.2 537.2,1911 946.9,1911.8 1595.5,2208.4 1148.7,2280.2 1059,2647 649.3,2647.8 0.8,2944.4 "></polyline>
      </svg>

      <!--01 设计-->
      <section class="scope">
        <p class="number">01</p>
        <div class="title">
          <h1>产品设计方案</h1>
          <h6>出色的产品设计方案出色的产品设计方案出色的产品设计方案出色的产品设计方案出色的产品设计方案出色的产品设计方案</h6>
        </div>
        <img class="scope_img" src="http://oy158wtwk.bkt.clouddn.com/illus-spotix-01-1-707x700.png"/>
      </section>

      <!--02 网站开发-->
      <section class="scope2">
        <p class="number">02</p>
        <div class="title">
          <h1>网站开发</h1>
          <h6>出色的产品设计方案出色的产品设计方案出色的产品设计方案出色的产品设计方案出色的产品设计方案出色的产品设计方案</h6>
        </div>
        <img class="scope_img" src="http://oy158wtwk.bkt.clouddn.com/illus-spotix-00-1.png"/>
      </section>

      <!--03 小程序开发-->
      <section class="scope3">
        <p class="number">03</p>
        <div class="title">
          <h1>小程序开发</h1>
          <h6>出色的产品设计方案出色的产品设计方案出色的产品设计方案出色的产品设计方案出色的产品设计方案出色的产品设计方案</h6>
        </div>
        <img class="scope_img" src="http://oy158wtwk.bkt.clouddn.com/illus-stat.png"/>
      </section>

      <!--跳转案例-->
      <section class="case">
        <p>我们的客户案例</p>
        <p class="case_button">案例</p>
      </section>
    </section>

    <!--底部-->
    <v-footer></v-footer>

  </div>
</template>

<script>
  import headerNav from '~/components/Nav.vue'
  import bgBody from '~/components/Bg_body.vue'
  import vFooter from '~/components/Footer.vue'

  export default {
    data() {
      return {}
    },
    components: {
      headerNav,
      bgBody,
      vFooter
    },
    methods: {},
    mounted() {
      var c = document.getElementById("downCanvas2"), cxt = c.getContext("2d");
      cxt.beginPath();
      cxt.moveTo(5, 20);
      cxt.lineTo(20, 35);
      cxt.lineTo(35, 20);
      cxt.lineWidth = 3;
      cxt.strokeStyle = "#ffffff";
      cxt.lineCap = 'round';
      cxt.lineJoin = "round";
      cxt.stroke();
    }
  }
</script>

<style>

  .main {
    position: relative;
    z-index: 100;
  }

  /*全局曲线*/
  .line {
    position: absolute;
    height: 100%;
    width: auto;
    top: 0;
    left: 0;
    opacity: 0.4;
  }

  .line * {
    fill: none;
    stroke: #FFF;
    stroke-width: 4;
    stroke-linejoin: round;
    stroke-miterlimit: 10;
  }

  /*曲线End*/

  .content > h1 {
    font-weight: bolder;
    font-size: 60px;
    color: #ffffff;
    text-align: center;
    margin-bottom: 20px;
  }

  .content > h6 {
    font-weight: 200;
    font-size: 22px;
    color: #ffffff;
    width: 700px;
    text-align: center;
    margin: 0 auto;
  }

  .main_img {
    display: block;
    margin: 0 auto;
  }

  /*我们的项目范围*/
  .home {
    position: relative;
    width: 1080px;
    height: 2150px;
    margin: 0 auto;
  }

  /*01*/
  .scope {
    width: 1080px;
    height: 600px;
    margin: 0 auto;
    position: relative;
  }

  .scope .number {
    position: absolute;
    font-size: 8em;
    font-weight: bolder;
    color: #ffffff;
    opacity: 0.4;
    z-index: 2;
  }

  .scope .title {
    float: left;
  }

  .scope .title > h1 {
    font-weight: bolder;
    font-size: 40px;
    color: #ffffff;
    margin-top: 150px;
    margin-bottom: 20px;
  }

  .scope .title > h6 {
    font-weight: 100;
    font-size: 20px;
    color: #ffffff;
    width: 400px;
    font-family: PingFangSC-Regular;
    margin-left: 50px;
  }

  .scope .scope_img {
    display: block;
    float: right;
    width: 480px;
    position: absolute;
    right: 0;
    top:100px;
  }

  /*01 end*/

  /*02*/
  .scope2 {
    width: 1080px;
    height: 600px;
    margin: 0 auto;
    position: relative;
  }

  .scope2 .number {
    position: absolute;
    font-size: 8em;
    font-weight: bolder;
    color: #ffffff;
    opacity: 0.4;
    z-index: 2;
    right: 0;
  }

  .scope2 .title {
    float: right;
  }

  .scope2 .title > h1 {
    font-weight: bolder;
    font-size: 40px;
    color: #ffffff;
    margin-top: 150px;
    margin-bottom: 20px;
    margin-left: 80px;
  }

  .scope2 .title > h6 {
    font-weight: 100;
    font-size: 20px;
    color: #ffffff;
    width: 400px;
    font-family: PingFangSC-Regular;
    margin-left: 50px;
  }

  .scope2 .scope_img {
    display: block;
    float: right;
    width: 700px;
    position: absolute;
    left: -100px;
  }

  /*02 end*/

  /*03*/
  .scope3 {
    width: 1080px;
    height: 600px;
    margin: 0 auto;
    position: relative;
  }

  .scope3 .number {
    position: absolute;
    font-size: 8em;
    font-weight: bolder;
    color: #ffffff;
    opacity: 0.4;
    z-index: 2;
  }

  .scope3 .title {
    float: left;
  }

  .scope3 .title > h1 {
    font-weight: bolder;
    font-size: 40px;
    color: #ffffff;
    margin-top: 200px;
    margin-bottom: 20px;
  }

  .scope3 .title > h6 {
    font-weight: 100;
    font-size: 20px;
    color: #ffffff;
    width: 400px;
    font-family: PingFangSC-Regular;
    margin-left: 50px;
  }

  .scope3 .scope_img {
    display: block;
    float: right;
    width: 600px;
    position: absolute;
    right: 50px;
  }

  /*03 end*/

  /*去案例*/
  .case > p {
    font-size: 2em;
    font-weight: bolder;
    color: #fff;
    text-align: center;
    position: relative;
    top: 50px;
  }

  .case_button {
    transition: all 0.7s cubic-bezier(0.455, 0.03, 0.515, 0.955);
    left: 0;
    background: -webkit-linear-gradient(120deg, #e26e36 0%, #e13a22 40%, #e26e36 70%, #e13a22 100%);
    font-size: 1em !important;
    width: 300px;
    height: 50px;
    line-height: 50px;
    text-align: center;
    border-radius: 30px;
    margin: 100px auto;
  }

  .case_button:hover {
    width: 350px;
    /*background: -webkit-linear-gradient(330deg, #e26e36 0%, #e13a22 40%, #e26e36 70%, #e13a22 100%);*/
  }
</style>
