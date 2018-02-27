<template>
  <div>
    <!--导航-->
    <header-nav></header-nav>
    <!--背景-->
    <bg-body></bg-body>

    <!--案例研究-->
    <section class="scope">
      <div class="title">
        <h1>案例研究</h1>
        <h6 class="h6">为客户部署的解决方案</h6>
      </div>
      <img class="scope_img" src="../static/img/illus-case-studies-1.png"/>
    </section>

    <!--锚点链接-->
    <div id="down3">
      <canvas id="downCanvas3" width="50" height="50">你的浏览器不支持canvas，请下载更新版本的浏览器
      </canvas>
    </div>

    <!--案例-->
    <section class="price">
      <ul>
        <li>
          <img @click="onDetail()" src="../static/img/tellmycity.jpg"/>
          <p class="price_name">卡蒂尼珠宝</p>
          <p class="price_text">在线购买BOX、珠宝凭借平台</p>
        </li>
        <li class="li2">
          <img src="../static/img/rbc-1.jpg"/>
          <p class="price_name">积分商城</p>
          <p class="price_text">通过游戏、购买商品获取积分，并通过积分获得商品优惠资格</p>
        </li>

      </ul>
      <ul class="ul2">
        <li>
          <img src="../static/img/scet-1.jpg"/>
          <p class="price_name">工商银行BBS</p>
          <p class="price_text">工商银行珠海分行，行内BBS</p>
        </li>
        <li class="li2_2">
          <img src="../static/img/rbc-2.jpg"/>
          <p class="price_name">定了么家具</p>
          <p class="price_text">提供在线定制家具服务</p>
        </li>
      </ul>
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
    methods: {
      onDetail(){
        this.$router.push({path:'/CaseDetail'})
      }
    },
    mounted() {
      var c = document.getElementById("downCanvas3"), cxt = c.getContext("2d");
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
    width: 550px;
    position: absolute;
    right: -100px;
    top: -50px;
  }

  /*01 end*/

  /*价值*/
  .price {
    width: 1080px;
    height: 1500px;
    margin: 0 auto;
    position: relative;
  }

  .price > ul {
    display: flex;
  }

  .price > ul > li {
    flex: 1;
    font-size: 40px;
    font-weight: bolder;
    color: #FFFFFF;
    text-align: center;
  }

  .price > ul .li2 {
    margin-top: 150px;
  }

  .price .ul2 {
    margin-top: -100px;
  }

  .price > ul .li2_2 {
    margin-top: 150px;
  }

  .price > ul > li > img {
    width: 350px;
    border-radius: 100%;
    margin-top: 110px;
    margin-bottom: 50px;
    border: 10px solid rgba(155, 155, 155, 0.2);
    box-shadow: 0px 0px 10px 15px rgba(0, 0, 0, 0.1);
  }

  .price > ul > li > .price_name {
    font-size: 25px;
  }

  .price > ul > li > .price_text {
    font-size: 18px;
    font-weight: 300;
    width: 400px;
    margin: 20px auto;
    line-height: 30px;
  }

</style>
