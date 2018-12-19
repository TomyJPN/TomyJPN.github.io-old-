<template>
  <div class="main">
    <section class="contents">
      <my-header />
      <div
        v-if="showNum===1"
        class="index">Tomy's Portfolio Site</div>
      <div v-if="showNum===2"><profile class="item"/></div>
      <!--div v-if="showNum===3"><Works class="item"/></div-->
      <div v-if="showNum===4"><Works class="item"/></div>
      <div v-if="showNum===5"><Links class="item"/></div>

    </section>
    <!--my-footer></my-footer-->
  </div>
</template>

<script>
  import MyHeader from '~/components/header.vue'
  import MyFooter from '~/components/footer.vue'
  import Profile from '~/components/profile.vue'
  import Works from '~/components/works.vue'
  import Links from '~/components/links.vue'

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

  document.onscroll = function(e){
    this.position = document.documentElement.scrollTop || document.body.scrollTop;
  }

</script>

<style>
  .main{
    background-color: darkslategray;
  }

  .contents {
    height: 100vh;
    background-color: darkslategray;
    color: whitesmoke;
  }

  .index{
    padding-top: 30vh;
    text-align: center;
    /*align-items: center;*/
    font-size: 50pt;
  }

  .item{
    background-color: #F5F5F5;
    color: #3d3d3d;
    margin-top: 30px;
    margin-left: 30px;
    margin-right: 30px;
    border-radius:5px;
    padding:20px 20px 20px 20px;
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

