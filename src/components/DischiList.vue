<template>
<div class="container">
    <div class="dischi-container">
        <Disco v-for="(element, index) in selectDiscs" :key="index" :details="element" />
    </div>
    <!-- {{selectDiscs}} -->
</div>  
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import axios from 'axios';
import Disco from "./Disco.vue";

export default {
  name: "DischiList",
  components: {
    Disco,
    
  },
  props: {
      genere: String
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
    },

    computed: {
        // ritorna un array dei dischi filtrati
        selectDiscs: function (){
            let newDiscs
            if (this.genere !== "all" ) {
                    newDiscs = this.disks.filter((element) =>{
                    return element.genre.toLowerCase() === this.genere
                }
             )
            }else{
                newDiscs = this.disks
            }
            console.log(newDiscs);
            return newDiscs
        }
    }
    
};


</script>

<style  >

    .dischi-container{
        width: 70%;
        margin: auto;
        display: flex;
        flex-wrap: wrap;
        padding: 20px 0px;
    }

</style>