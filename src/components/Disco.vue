<template>
  
      
          <div class="single-disco">
              <div class="disco-img">
                  <img :src="details.poster" alt="">
              </div>
              <div class="disco-title white">{{ details.title }}</div>
              <div class="disco-dati">
                  <div class="artist grey">{{ details.author }}</div>
                  <div class="date grey">{{ details.year }}</div>
              </div>
          </div>
      
  
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
  

export default {
  name: "Disco",
  props: {
        details: Object
    }
};
</script>


<style >

    .container{
        background-color: #1e2d3b;
    }

    .single-disco{
        width: calc(100% / 5 - 20px);
        background-color: #2e3a46;
        padding: 10px;
        text-align: center;
        margin: 10px;
    }

    .white{
        color: white;
    }

    .grey{
        color: #6c6e71;
    }

    .disco-dati{
        padding: 10px 0px;
    }

</style>