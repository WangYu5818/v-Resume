<template>
  <div class="container" id="app">
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style>
.container{
  width:100%;
  max-width:1280px;
  margin: 0 auto;
}
</style>
