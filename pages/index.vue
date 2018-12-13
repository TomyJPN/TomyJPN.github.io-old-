<template>
  <div class="main">
    <my-header></my-header>
  <section class="container">
    Tomy's Portfolio Site
    <!--<div>
      <app-logo/>
      <h1 class="title">
        tomyport
      </h1>
      <h2 class="subtitle">
        tomy's portfolio site.(Under construction)
              </h2>
      <div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          class="button--green">Documentation</a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          class="button--grey">GitHub</a>
      </div>
    </div>-->
  </section>
    <my-footer></my-footer>
  </div>
</template>

<script>
import AppLogo from '~/components/AppLogo.vue'
import MyHeader from '~/components/header.vue'
import MyFooter from '~/components/footer.vue'

export default {
  components: {
    AppLogo,
    MyHeader,
    MyFooter
  }
}
</script>

<style>
  .main{
    width: 100%;
    height: 100%;
    min-height: 100%;
  }

.container {
  min-height: 90vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background-color: darkslategray;
  font-size: 50pt;
  color: whitesmoke;
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

