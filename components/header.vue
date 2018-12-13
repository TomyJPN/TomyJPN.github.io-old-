<template>
  <div class="main">
    <router-link tag="div" to="/">
    </router-link>
    <div class="header-navi">
      <ul>
        <router-link to="/" class="square_btn">top</router-link>
        <router-link to="/profile" class="square_btn">profile</router-link>
        <router-link to="/language" class="square_btn">language</router-link>
        <router-link to="/works" class="square_btn">works</router-link>
        <router-link to="/link" class="square_btn">link</router-link>
      </ul>
    </div>
  </div>
</template>

<script>
    export default {
        name: "myheader"
    }
</script>

<style scoped>
  /* 今回は最低限のスタイルのみ用意しました */
  .on {
    color: orange;
  }
  .main{
    background-color: #fff;
    position: sticky;
    height: 70px;
    top: 0;
    padding-top:8px;
    font-size:18pt;
  }
  ul {
    display: flex;
    justify-content: space-around;
  }
  .square_btn{
    position: relative;
    display: inline-block;
    font-weight: bold;
    padding: 0.25em 0;
    text-decoration: none;
    color:  darkslategray;
  }
  .square_btn:before{
    position: absolute;
    content: '';
    width: 100%;
    height: 4px;
    top:100%;
    left: 0;
    border-radius: 3px;
    background: darkslategray;
    transition: .2s;
  }
  .square_btn:hover:before {
    top: -webkit-calc(100% - 3px);
    top: calc(100% - 3px);
  }
</style>
