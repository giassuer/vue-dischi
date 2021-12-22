<template>
  <div id="app">
    <Header />
    <DischiList />
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
  import Header from "./components/Header.vue";
  import DischiList from "./components/DischiList.vue";

export default {
  name: "App",
  components: {
    Header,
    DischiList
  },
};
</script>

<style >

  *{
      margin: 0;
      padding: 0;
      box-sizing: border-box;
  }

  img{
      width: 100%;
  }


</style>
