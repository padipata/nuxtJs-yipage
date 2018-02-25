<template>
  <div class="header">
    <p class="logo">一页科技</p>
    <ul class="nav">
      <nuxt-link to="/">
        <li>Home</li>
      </nuxt-link>
      <nuxt-link to="/Case">
        <li>案例</li>
      </nuxt-link>
      <nuxt-link to="/About">
        <li>团队</li>
      </nuxt-link>
      <nuxt-link to="/">
        <li>定制</li>
      </nuxt-link>
    </ul>
  </div>
</template>

<style>
  .header {
    width: 1080px;
    height: 200px;
    margin: 0 auto;
    position: relative;
    z-index: 100;
  }

  .header .logo {
    font-weight: bolder;
    font-size: 35px;
    color: #ffffff;
    line-height: 200px;
    float: left;
  }

  .header .nav {
    width: 500px;
    display: flex;
    float: right;
    line-height: 200px;
  }

  .header .nav > li {
    flex: 1;
    text-align: center;
    color: #ffffff;
    font-size: 23px;
  }

  .header .nav a {
    display: block;
    color: #ffffff;
    flex: 1;
    text-align: right;
  }

  .header .nav a:hover {
    color: #dbe1ec;
  }
</style>
