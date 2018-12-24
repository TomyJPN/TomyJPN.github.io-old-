<template>

  <div class="main">
    <my-header />
    <div
      v-if="showNum===1"
      class="index">Tomy's Portfolio Site
      <div class="sub">～Toriaezu Making～</div>
    </div>
    <div v-if="showNum===2"><profile class="item"/></div>
    <!--div v-if="showNum===3"><Works class="item"/></div-->
    <div v-if="showNum===4"><Works class="item"/></div>
    <div v-if="showNum===5"><Links class="item"/></div>

  </div>
  <!--my-footer></my-footer-->

</template>

<script>
  import MyHeader from '~/components/header.vue'
  import MyFooter from '~/components/footer.vue'
  import Profile from '~/components/profile.vue'
  import Works from '~/components/works.vue'
  import Links from '~/components/links.vue'
  import Vue from 'vue'
  import VueAnalytics from 'vue-analytics'

  Vue.use(VueAnalytics, {
    id: 'UA-131283692-1'
  })

  document.title="Tomy's Portfolio site"

  export default {
    components: {
      MyHeader,
      MyFooter,
      Profile,
      Works,
      Links
    },
    data(){
      return {
        showNum: 1
      }
    }
  }



</script>

<style>
  .main {
    /*height: 100vh;*/
    bottom: 0;
    margin: auto;
    background-color: darkslategray;
    color: whitesmoke;
  }

  .index{
    margin-top: 20vh;
    text-align: center;
    /*align-items: center;*/
    font-size: 50pt;
  }

  .item{
    background-color: #F5F5F5;
    color: #3d3d3d;
    margin-top: 30px;
    margin-bottom: 30px;
    margin-left: 5%;
    margin-right: 5%;
    border-radius:5px;
    padding:20px 20px 20px 20px;
  }

  .sub{
    font-size: 24px;
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

