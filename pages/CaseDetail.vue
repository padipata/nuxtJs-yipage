<template>
  <div>
    <!--导航-->
    <header-nav></header-nav>
    <!--背景-->
    <bg-body></bg-body>

    <!--案例研究-->
    <section class="scope">
      <div class="title">
        <h1>卡蒂尼珠宝</h1>
        <h6 class="h6">在线购买BOX、珠宝凭借平台</h6>
      </div>
      <img class="scope_img" src="http://oy158wtwk.bkt.clouddn.com/tellmycity.jpg"/>
    </section>

    <!--锚点链接-->
    <div id="down4">
      <canvas id="downCanvas4" width="50" height="50">你的浏览器不支持canvas，请下载更新版本的浏览器
      </canvas>
    </div>

    <!--技术-->
    <section class="personal">
      <div class="personal_main">
        <p class="personal_title">技术说明</p>
        <p class="type_left">在考虑产品快速迭代、用户体验、安全性能的情况下，使用Vue来实现SPA单页应用是非常合适的</p>
        <div class="type_right">
          <p class="type_title">技术使用</p>
          <p class="type_text">Vue2.0</p>
          <p class="type_title2">客户类别</p>
          <p class="type_text2">私营服务</p>
        </div>
      </div>
    </section>

    <!--价值-->
    <section class="price">
      <p class="price_title">客户需求</p>
      <p class="price_title2">挑战</p>
      <p class="xuqiu">与客户沟通</p>
      <img class="scope_img" src="http://oy158wtwk.bkt.clouddn.com/montoban.jpg"/>
    </section>

    <!--解决方案-->
    <section class="section-arrow">
      <section class="personal2">
        <div class="personal_main">
          <p class="personal_title">我们提出了</p>
          <p class="personal_title2">部署的解决方案</p>
          <div class="type_left">
            <p>展望未来，尝试创新，塔恩加龙省这座最大的城市自然选择了TELLMYCITY®与其公民进行交流。</p>
            <p>正如蒙托邦市市长BrigitteBarèges所解释的那样，“在蒙托邦，我们置身于可持续创新的视角，以迎接未来城市的真正挑战。我们多年来一直致力于通过智能系统提供优质的公共服务。</p>
            <p>一页科技开发的创新应用程序自2017年5月开始部署，已经很快证明自己已经有超过5000个报告。在不到一年的时间里，报告的平均处理时间从平均60天增加到现在不到4天。</p>
          </div>
          <div class="type_right">
            <img src="http://oy158wtwk.bkt.clouddn.com/Montauban-3-760x700.jpg"/>
          </div>
        </div>
      </section>
    </section>


    <!--底部-->
    <v-footer></v-footer>
  </div>
</template>

<script type="text/ecmascript-6">
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
      var c = document.getElementById("downCanvas4"), cxt = c.getContext("2d");
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

<style scoped>
  /*01*/
  .scope {
    width: 1080px;
    height: 400px;
    margin: 0 auto;
    position: relative;
  }

  .scope .title {
    float: left;
  }

  .scope .title > h1 {
    font-weight: bolder;
    font-size: 50px;
    color: #ffffff;
    margin-top: 50px;
    margin-bottom: 20px;
  }

  .scope .title > .h6 {
    font-weight: 100;
    font-size: 25px;
    color: #ffffff;
    width: 550px;
    font-family: PingFangSC-Regular;
    margin-left: 0;
  }

  .scope .scope_img {
    display: block;
    position: absolute;
    right: -50px;
    top: -100px;
    width: 450px;
    border-radius: 100%;
    margin-top: 110px;
    margin-bottom: 50px;
    border: 10px solid rgba(155, 155, 155, 0.2);
    box-shadow: 0px 0px 10px 15px rgba(0, 0, 0, 0.1);

  }

  /*01 end*/

  /*技术说明*/
  .personal {
    width: 100%;
    height: 550px;
    background: #FFFFFF;
    position: relative;
    z-index: 200;
    margin-top: 100px;
  }

  .personal .personal_main {
    width: 1080px;
    height: 100%;
    margin: 0 auto;
  }

  .personal .personal_title {
    font-weight: 400;
    font-size: 25px;
    padding-top: 50px;
  }

  .personal .type_left {
    float: left;
    font-weight: bolder;
    font-size: 30px;
    width: 600px;
    margin-top: 100px;
  }

  .personal .type_right {
    float: right;
    margin-right: 100px;
  }

  .personal .type_right .type_title {
    margin-top: 100px;
    font-weight: 600;
    font-size: 18px;
    margin-bottom: 5px;
  }

  .personal .type_right .type_text {
    font-weight: 200;
    font-size: 20px;
  }

  .personal .type_right .type_title2 {
    margin-top: 70px;
    font-weight: 600;
    font-size: 18px;
    margin-bottom: 5px;
  }

  .personal .type_right .type_text2 {
    font-weight: 200;
    font-size: 20px;
  }

  /*客户需求*/
  .price {
    width: 1080px;
    height: 900px;
    margin: 0 auto;
    position: relative;
  }

  .price_title {
    text-align: center;
    color: rgba(255, 255, 255, 0.6);
    font-weight: bolder;
    font-size: 16px;
    margin-top: 100px;
  }

  .price_title2 {
    text-align: center;
    color: rgba(255, 255, 255, 1);
    font-weight: bolder;
    font-size: 55px;
    margin-top: 10px;
  }

  .price .xuqiu {
    position: relative;
    color: #FFFFFF;
    font-size: 30px;
    font-weight: 400;
    top: 50px;
    left: 150px;
  }

  .price .xuqiu::before {
    content: '“';
    font-size: 300px;
    line-height: 1em;
    opacity: 0.2;
    letter-spacing: -0.05em;
    position: absolute;
    font-family: sans-serif;
    top: 0;
    font-weight: bolder;
    left: -50px;
    -webkit-transform: translate3d(-50%, -25%, 0);
    transform: translate3d(-50%, -25%, 0);
    -webkit-transition-delay: 0.3s;
    transition-delay: 0.3s;
  }

  .price .scope_img {
    display: block;
    position: absolute;
    left: 0;
    right: 0;
    margin: auto;
    width: 500px;
    border-radius: 100%;
    margin-top: 110px;
    margin-bottom: 50px;
    border: 10px solid rgba(155, 155, 155, 0.2);
    box-shadow: 0 0 10px 15px rgba(0, 0, 0, 0.1);
  }

  /*解决*/
  .section-arrow {
    color: #252525;
    padding-top: 40px;
    margin-top: 60px;
    background: #FFF;
    padding-bottom: 50px;
    margin-bottom: 200px;
    position: relative;
  }

  .section-arrow:before {
    width: 50%;
    height: 50px;
    content: '';
    position: absolute;
    bottom: 100%;
    right: 50%;
    -webkit-transform: skewX(45deg);
    -ms-transform: skewX(45deg);
    transform: skewX(45deg);
    background: #FFF;
    -webkit-transform-origin: bottom right;
    -ms-transform-origin: bottom right;
    transform-origin: bottom right;
  }

  .section-arrow:after {
    width: 50%;
    height: 50px;
    content: '';
    position: absolute;
    bottom: 100%;
    left: 50%;
    -webkit-transform: skewX(-45deg);
    -ms-transform: skewX(-45deg);
    transform: skewX(-45deg);
    background: #FFF;
    -webkit-transform-origin: bottom left;
    -ms-transform-origin: bottom left;
    transform-origin: bottom left;
  }

  .personal2 {
    width: 100%;
    height: 600px;
    background: #FFFFFF;
    position: relative;
    z-index: 200;
  }

  .personal2 .personal_main {
    width: 1180px;
    height: 100%;
    margin: 0 auto;
  }

  .personal2 .personal_title {
    font-weight: 400;
    font-size: 18px;
    padding-top: 50px;
    text-align: center;
  }

  .personal2 .personal_title2 {
    font-weight: 900;
    font-size: 50px;
    text-align: center;
  }

  .personal2 .type_left {
    float: left;
    font-weight: 300;
    font-size: 16px;
    width: 650px;
    margin-top: 50px;
  }

  .personal2 .type_left > p {
    margin-bottom: 50px;
  }

  .personal2 .type_right {
    float: right;
  }

  .personal2 .type_right > img {
    width: 520px;
  }


</style>
