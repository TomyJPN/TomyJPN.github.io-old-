<template>
  <div class="main">
    <div class="header-navi">

      <ul>
        <button 
          class="square_btn" 
          @click="index">top</button>
        <button 
          to="/" 
          class="square_btn" 
          @click="profile">profile</button>
        <!--button
          to="/" 
          class="square_btn" 
          @click="language">language</button-->
        <button 
          to="/"
          class="square_btn" 
          @click="works">works</button>
        <button 
          to="/"
          class="square_btn" 
          @click="link">link</button>
      </ul>
    </div>
  </div>
</template>

<script>
    export default {
        name: "Myheader",
      methods:{
        index(){
          this.$parent.showNum=1;
        },
        profile() {
          this.$parent.showNum = 2;
        },
        language(){
          this.$parent.showNum = 3;
        },
        works(){
          this.$parent.showNum = 4;
        },
        link(){
          this.$parent.showNum = 5;
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
    background-color: #c4dcc4;
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
