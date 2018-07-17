<template>
  <div id="app">
    <!--  加载过一次就不需要重新渲染 -->
    <keep-alive exclude="Detail">
      <router-view/>
    </keep-alive>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style></style>
