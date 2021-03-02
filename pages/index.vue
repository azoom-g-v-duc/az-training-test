<template>
  <div class="container">
    <component-header></component-header>
    <component-hot-news></component-hot-news>
    <component-related-news></component-related-news>
  </div>
</template>

<script>
export default {}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
