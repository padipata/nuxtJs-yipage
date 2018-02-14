<template>
  <section class="container">
    <div>
      <h1 class="title">
        nuxt-yipage
      </h1>
      <h2 class="subtitle">
        Padipata
      </h2>
      <div class="links">
        <p class="button--green" @click="onCase()">案例</p>
        <p class="button--grey" @click="onAbout()">关于我们</p>
      </div>
    </div>
  </section>
</template>

<script>

export default {
  data() {
    return {}
  },
  components: {

  },
  methods: {
    onCase(){
      this.$router.push({path:'/Case'})
    },
    onAbout(){
      this.$router.push({path:'/About'})
    }
  },
  mounted() {

  }
}
</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
