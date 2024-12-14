<template>
  <div id="app">
    <h1></h1>
    <button @click="goToExternalSite">  کلیک کنید </button>
  </div>
</template>

<script>
export default {
  name: 'App',
  methods: {
    goToExternalSite() {
      let urlParams = new URLSearchParams(window.location.search);

      const code =(urlParams.get('code'));
      window.open("https://gnaf2.post.ir/pdf/postalcodes/plate/" + code, '_blank');
    }
  }
}
</script>

<style>
#app {
  text-align: center;
  margin-top: 50px;
}
button {
  color: crimson;
  padding: 10px 20px;
  font-size: 16px;
}
</style>
