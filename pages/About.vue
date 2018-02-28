<template>
  <div>
    <!--导航-->
    <header-nav></header-nav>

    <!--背景-->
    <bg-body></bg-body>

    <!--我们是谁-->
    <section class="scope">
      <div class="title">
        <h1>我们是谁？</h1>
        <h6 class="h6">作为互联网解决方案机构，一页科技在网站开发和安全研究领域提供量身定制的支持。</h6>
      </div>
      <img class="scope_img" src="../static/img/illus-job.png"/>
    </section>

    <!--锚点链接-->
    <div id="down">
      <canvas id="downCanvas" width="50" height="50">你的浏览器不支持canvas，请下载更新版本的浏览器
      </canvas>
    </div>

    <!--公司概况-->
    <section class="number">
      <ul>
        <li>
          <p>10</p>
          <p>成功案例</p>
          <p>我们的技术和解决方案是成功的保障</p>
        </li>
        <li>
          <p>50</p>
          <p>解决方案</p>
          <p>我们有独到的互联网产品解决方案</p>
        </li>
        <li>
          <p>1000000+</p>
          <p>用户数量</p>
          <p>我们以优越的用户体验以及产品稳定性给客户带来大量的用户</p>
        </li>
      </ul>
    </section>

    <!--核心成员-->
    <section class="personal">
      <div class="personal_main">
        <p class="personal_title">核心成员</p>
        <ul>
          <li>
            <img src="../static/img/Jan_Tavart-440x440.jpg"/>
            <p class="personal_name">Edison</p>
            <p class="personal_wei">CEO</p>
          </li>
          <li>
            <img src="../static/img/Renaud_Prouveur-440x440.jpg"/>
            <p class="personal_name">Padipata</p>
            <p class="personal_wei">项目经理</p>
          </li>
          <li>
            <img src="../static/img/Olivier_Ricca-440x440.jpg"/>
            <p class="personal_name">Agger</p>
            <p class="personal_wei">技术主管</p>
          </li>
        </ul>
      </div>
    </section>

    <!--价值-->
    <section class="price">
      <p class="price_title">深圳市一页科技有限公司</p>
      <p class="price_title2">我们的价值</p>
      <ul>
        <li>
          <img src="../static/img/logo-icon.svg"/>
          <p class="price_name">独立性</p>
          <p class="price_text">一页科技提出的技术100％由内部开发</p>
        </li>
        <li>
          <img src="../static/img/diplome.svg"/>
          <p class="price_name">经验</p>
          <p class="price_text">我们的团队成员一共完成来自公共或私营部门的50多名客户</p>
        </li>
      </ul>
      <ul>
        <li>
          <img src="../static/img/light.svg"/>
          <p class="price_name">创新</p>
          <p class="price_text">公司致力于创新型产品研发</p>
        </li>
        <li>
          <img src="../static/img/crown.svg"/>
          <p class="price_name">技术</p>
          <p class="price_text">我们因为团队成员技术得到客户的认可</p>
        </li>
      </ul>
      <ul>
        <li>
          <img src="../static/img/shield.svg"/>
          <p class="price_name">安全</p>
          <p class="price_text">一页科技的技术独立性保证了客户的安全和数据保护</p>
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
    methods: {},
    mounted() {
      var c = document.getElementById("downCanvas"), cxt = c.getContext("2d");
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
    font-size: 20px;
    color: #ffffff;
    width: 550px;
    font-family: PingFangSC-Regular;
    margin-left: 0;
  }

  .scope .scope_img {
    display: block;
    width: 700px;
    position: absolute;
    right: -150px;
    top: -120px;
  }

  /*01 end*/

  .number {
    width: 1080px;
    height: 500px;
    margin: 0 auto;
    position: relative;
  }

  .number > ul {
    width: 100%;
    display: flex;
  }

  .number > ul > li {
    flex: 1;
    text-align: center;
    color: #FFFFFF;
    font-weight: bolder;
    font-size: 1.2em;
  }

  .number > ul > li > p:nth-child(1) {
    font-weight: 300;
    font-size: 1.7em;
    margin-top: 150px;
    margin-bottom: 30px;
  }

  .number > ul > li > p:nth-child(3) {
    font-weight: 200;
    font-size: 16px;
    margin-top: 20px;
  }

  /*成员*/
  .personal {
    width: 100%;
    height: 520px;
    background: #FFFFFF;
    position: relative;
    z-index: 200;
  }

  .personal_main {
    width: 1080px;
    height: 100%;
    margin: 0 auto;
  }

  .personal_title {
    font-weight: bolder;
    font-size: 30px;
    padding-top: 30px;
  }

  .personal_main > ul {
    display: flex;
  }

  .personal_main > ul > li {
    flex: 1;
    text-align: center;
  }

  .personal_main > ul > li > img {
    width: 250px;
    border-radius: 100%;
    display: block;
    margin: 50px auto 0 auto;
    border: 10px solid #eeeeee;
    box-shadow: 0px 0px 30px 5px rgba(0, 0, 0, 0.2);
  }

  .personal_main > ul > li .personal_name {
    margin-top: 30px;
    font-weight: bolder;
  }

  .personal_main > ul > li .personal_wei {
    margin-top: 10px;
    font-weight: 200;
    font-size: 15px;
    color: #666666;
  }

  /*价值*/
  .price {
    width: 1080px;
    height: 1200px;
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
    font-size: 50px;
    margin-top: 10px;
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

  .price > ul > li > img {
    height: 65px;
    margin-top: 110px;
    margin-bottom: 50px;
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
