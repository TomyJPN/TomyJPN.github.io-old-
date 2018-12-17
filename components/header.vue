<template>
  <div class="main">
    <div class="header-navi">
      <ul>
        <button v-on:click="index" class="square_btn">top</button>
        <button to="/" v-on:click="profile" class="square_btn">profile</button>
        <button to="/" v-on:click="language" class="square_btn">language</button>
        <button to="/" v-on:click="works" class="square_btn">works</button>
        <button to="/" v-on:click="link" class="square_btn">link</button>
      </ul>
    </div>
  </div>
</template>

<script>
    export default {
        name: "myheader",
        showNum:1,
      methods:{
        index(){
          this.$emit("index");
        },
        profile(){
          this.$emit("profile")},
        language(){
          this.$emit("language")
        },
        works(){
          this.$emit("works")
        },
        link(){
          this.$emit("link")
        }
      }
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
