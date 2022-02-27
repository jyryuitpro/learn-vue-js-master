<template>
  <header>
    <h1>Header</h1>
    <h1>{{ propsdata }}</h1>
  </header>
</template>

<script>
export default {
  name: "AppHeader",
  props: ['propsdata'],
}
</script>

<style scoped>

</style>