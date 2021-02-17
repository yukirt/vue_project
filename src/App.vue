<template>
  <div id='app'>
    <router-view />
  </div>
</template>

<script>
export default {
  name: 'App',
  created () {
    const api = `${process.env.APIPATH}/${process.env.CUSTOMPATH}/products`
    console.log(api)
    this.$http.get(api).then((response) => {
      console.log(response.data)
    })
  }
}
</script>

<style lang="scss">
@import "./assets/all";
</style>
