<template>
    <div class="main">
      <div class="about">
        <h2>profile</h2>
        <p>Toyota Masaya (a.k.a Tomy,Томиников)</p>
        <p>北九州工業高等専門学校 情報システムコース</p>
        <p>コンピュータ研究部 部長を経験</p>
        <h2>Like</h2>
        <p>ゲーム開発，創作，ミリタリー，サバゲー,にじさんじ</p>
        <h2>Language</h2>
        <p>C,C++,C#,JavaScript,HTML/CSS</p>
        <p>自然言語:Studying Japanese!</p>
        <h2>Word</h2>
        <p>Unity,DXlib,3D Modeling,Web,front-end</p>
      </div>
    </div>
</template>

<script>
    export default {
        name: "profile",
      data(){
          isActive:'1'
      },
      methods:{
          isSelect:function(num){
            this.isActive=num;
          }
      }
    }
</script>

<style scoped>

</style>
