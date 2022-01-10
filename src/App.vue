<template>
  <div id="app">
    <Header />
    <FilterDisc @selectDisc="selectDisc" />
    <DischiList :genere="genereValue" />
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
  import Header from "./components/Header.vue";
  import DischiList from "./components/DischiList.vue";
  import FilterDisc from "./components/FilterDisc.vue";

export default {
  name: "App",
  components: {
    Header,
    FilterDisc,
    DischiList
  },
  data: function(){
    return{
      genereValue: "all"
    }
  },
  methods: {
    selectDisc: function(value){
      this.genereValue = value
    }
  }
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
