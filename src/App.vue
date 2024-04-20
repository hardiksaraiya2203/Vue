<template>
  <div>hello {{Fname}} {{Mname}}</div>
  <div v-text="Lname"></div>
  <!-- error v-text will override the children   -->
  <p v-html="Price"></p>
  <!-- do not bind api data which causes easily vurnarable to hackers  -->

  <!-- binding attribute bool and id  -->
  <h1 v-bind:id="headerId">Heading</h1>
  <button v-bind:disabled="isDisabled">Bind</button>

</template>

<script>
export default {
  name: "App",
  data() {
    return {
      Fname: "Hardik",
      Lname: "Saraiya",
      Mname: "Umesh",
      Price: `<a href="#" onclick="alert('you are hacked')">Win a Price</a>`,
      headerId : "headerId",
      isDisabled : "true",
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
