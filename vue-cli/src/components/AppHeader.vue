<template>
  <header>
    <h1>Header</h1>
    <h1>{{ propsdata }}</h1>
    <button v-on:click="sendEvent">send</button>
  </header>
</template>

<script>
export default {
  name: "AppHeader",
  props: ['propsdata'],
  methods: {
    sendEvent: function () {
      this.$emit('renew');
    }
  }
}
</script>

<style scoped>

</style>