<template>
  <div class="main">
    <my-header />
    <section class="contents">
      <div
        v-if="showNum===1"
        class="index">Tomy's Portfolio Site</div>
      <div v-if="showNum===2"><profile class="item">profile</profile></div>
      <div v-if="showNum===3">a</div>
      <div v-if="showNum===4">sfae</div>
    </section>
    <!--my-footer></my-footer-->
  </div>
</template>

<script>
  import MyHeader from '~/components/header.vue'
  import MyFooter from '~/components/footer.vue'
  import Profile from '~/components/profile.vue'

  export default {
    components: {
      MyHeader,
      MyFooter,
      Profile,

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
    height: 92vh;
    background-color: darkslategray;
    color: whitesmoke;
  }

  .index{
    padding-top: 30vh;
    text-align: center;
    align-items: center;
    font-size: 50pt;
    width: 100%;
  }

  .item{
    height: 80%;
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

