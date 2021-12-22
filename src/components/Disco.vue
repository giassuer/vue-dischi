<template>
  <div class="container">
      <div class="dischi-container">
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

    .dischi-container{
        width: 70%;
        margin: auto;
        display: flex;
        flex-direction: row;
    }

    .single-disco{
        width: calc(100% / 5);
        background-color: #2e3a46;
        padding: 10px;
        text-align: center;
    }

    .white{
        color: white;
    }

    .grey{
        color: #6c6e71;
    }

</style>