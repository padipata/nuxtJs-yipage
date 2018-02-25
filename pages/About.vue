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
        <h6>作为互联网解决方案机构，一页科技在网站开发和安全研究领域提供量身定制的支持。</h6>
      </div>
      <img class="scope_img" src="../static/img/illus-job.png"/>
    </section>

    <!--锚点链接-->
    <div id="down">
      <canvas id="downCanvas" width="50" height="50">你的浏览器不支持canvas，请下载更新版本的浏览器
      </canvas>
    </div>



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
    height: 350px;
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

  .scope .title > h6 {
    font-weight: 100;
    font-size: 15px;
    color: #ffffff;
    width: 550px;
    font-family: PingFangSC-Regular;
  }

  .scope .scope_img {
    display: block;
    width: 700px;
    position: absolute;
    right: -150px;
    top: -120px;
  }

  /*01 end*/

  @-moz-keyframes myMove {
    0% {
      padding-top: 30px;
    }
    100% {
      padding-top: 50px;
    }
  }

  @-webkit-keyframes myMove {
    0% {
      padding-top: 30px;
    }
    100% {
      padding-top: 50px;
    }
  }

  @-o-keyframes myMove {
    0% {
      padding-top: 30px;
    }
    100% {
      padding-top: 50px;
    }
  }

  @keyframes myMove {
    0% {
      padding-top: 30px;
    }
    100% {
      padding-top: 50px;
    }
  }

  #down {
    position: relative;
    z-index: 200;
    text-align: center;
    height: 50px;
    -moz-animation: myMove 1s linear infinite alternate;
    -webkit-animation: myMove 1s linear infinite alternate;
    -o-animation: myMove 1s linear infinite alternate;
    animation: myMove 1s linear infinite alternate;
  }

</style>
