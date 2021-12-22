<template>
    <div>
        <Disco v-for="(element, index) in disks" :key="index" :details="element" />
    </div>
  
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import axios from 'axios';
import Disco from "./Disco.vue";

export default {
  name: "DischiList",
  components: {
    Disco
    
  },
  data: function() {
        return {
            disks: [],
        };
    },
    created: function() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((response) => {
            this.disks = response.data.response;
        });
    }
};

</script>

<style scoped >

    

</style>