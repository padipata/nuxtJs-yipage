<template>
  <div>
    <!--导航-->
    <header-nav></header-nav>
    <!--背景-->
    <bg-body></bg-body>

    <!--案例研究-->
    <section class="scope">
      <div class="title">
        <h1>联系我们</h1>
        <h6 class="h6">项目信息？</h6>
        <h6 class="h6">我们见面吧！</h6>
      </div>
      <img class="scope_img" src="http://oy158wtwk.bkt.clouddn.com/corto-atout1.png"/>
    </section>

    <!--锚点链接-->
    <div id="down5">
      <canvas id="downCanvas5" width="50" height="50">你的浏览器不支持canvas，请下载更新版本的浏览器
      </canvas>
    </div>

    <!--联系我们-->
    <section class="personal">
      <div class="personal_main">
        <p class="personal_title">联系我们<i class="icon"></i></p>
        <p class="personal_title2">请填写您的信息</p>
        <div class="type_left">
          <p class="line"><span>您的姓名</span><input type="text"/></p>
          <p class="line"><span>联系方式</span><input type="text"/></p>
          <p class="line"><span>电子邮箱</span><input type="text"/></p>
          <p class="line"><span>项目信息</span><textarea class="more_text"></textarea></p>
        </div>
        <div class="type_right">
          <img src="http://oy158wtwk.bkt.clouddn.com/illus-contact2.png"/>
        </div>
      </div>
    </section>

    <!--联系地址-->
    <section class="price">
      <p class="price_title">我们的地址</p>
      <p class="price_title2">访问我们</p>
      <img class="scope_img" src="http://oy158wtwk.bkt.clouddn.com/montoban.jpg"/>
      <p class="site_name">湖北大厦</p>
      <p class="site_name2">详细地址：深圳市福田区湖北大厦xxx</p>
      <p class="site_phone">联系电话：+86 18814002160</p>
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
      var c = document.getElementById("downCanvas5"), cxt = c.getContext("2d");
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
    font-weight: 200;
    font-size: 30px;
    color: #ffffff;
    width: 550px;
    margin-left: 0;
  }

  .scope .scope_img {
    display: block;
    width: 300px;
    position: absolute;
    right: 50px;
    top: 0;
    transform: scaleX(-1);
  }

  /*01 end*/

  /*联系我们*/
  .personal {
    width: 100%;
    height: 1000px;
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
    font-size: 18px;
    color: #ffffff;
    width: 300px;
    height: 40px;
    line-height: 40px;
    background: #665757;
    border-radius: 50px;
    text-align: center;
    display: block;
    position: absolute;
    top: 100px;
  }

  .personal .personal_title .icon {
    position: absolute;
    width: 20px;
    height: 15px;
    background: url("../static/img/enveloppe.svg") no-repeat;
    background-size: 100%;
    margin: auto;
    top: 0;
    bottom: 0;
    left: 80px;
  }

  .personal .personal_title2 {
    padding-top: 250px;
    font-size: 40px;
    font-weight: bolder;
  }

  .personal .type_left {
    float: left;
    font-weight: bolder;
    font-size: 30px;
    width: 600px;
    margin-top: 100px;
    margin-left: 100px;
  }

  .personal .type_left .line {
    margin-bottom: 20px;
  }

  .personal .type_left .line > span {
    font-size: 20px;
    padding-right: 40px;
  }

  .personal .type_left .line > input {
    border: 3px solid #bbbbbb;
    padding: 10px;
    font-size: 20px;
    width: 400px;
  }

  .personal .type_left .line .more_text {
    border: 3px solid #bbbbbb;
    padding: 10px;
    font-size: 20px;
    width: 400px;
    height: 200px;
    outline: none;
    resize: none;
  }

  .personal .type_right {
    float: right;
    margin-top: -100px;
  }

  .personal .type_right img {
    width: 300px;
  }

  /*地址信息*/
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

  .price .scope_img {
    display: block;
    position: absolute;
    left: 0;
    right: 0;
    margin: auto;
    width: 500px;
    border-radius: 100%;
    margin-top: 50px;
    margin-bottom: 50px;
    border: 10px solid rgba(155, 155, 155, 0.2);
    box-shadow: 0 0 10px 15px rgba(0, 0, 0, 0.1);
  }

  .price .site_name {
    color: #FFFFFF;
    font-size: 30px;
    font-weight: 800;
    text-align: center;
    margin-top: 600px;
  }

  .price .site_name2 {
    color: #FFFFFF;
    font-size: 15px;
    font-weight: 400;
    text-align: center;
    margin-top: 10px;
  }

  .price .site_phone {
    color: #FFFFFF;
    font-size: 15px;
    font-weight: 400;
    text-align: center;
    margin-top: 10px;
  }

</style>
