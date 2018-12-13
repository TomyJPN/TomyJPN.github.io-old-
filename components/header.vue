<template>
  <main>
    <router-link tag="div" to="/">
    </router-link>
    <div class="header-navi">
      <ul>
        <router-link class="on" to="/">top</router-link>
        <router-link to="/profile">profile</router-link>
        <router-link to="/language">language</router-link>
        <router-link to="/works">works</router-link>
        <router-link to="/link">link</router-link>
      </ul>
    </div>
  </main>
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
</style>
