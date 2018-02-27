<template>
  <div>
    <!--导航-->
    <header-nav></header-nav>
    <!--背景-->
    <bg-body></bg-body>


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

    }
  }
</script>

<style scoped>

</style>
