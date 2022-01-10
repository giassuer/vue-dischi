<template>
    <div class="filter">
        <select @change="test" v-model="filterValue" name="" id="">
            <option value="all">all</option>
            <option value="rock">rock</option>
            <option value="pop">pop</option>
            <option value="dance">dance</option>
        </select>
    </div>
</template>

<script>

export default{
    name: "FilterDisc", 
    data: function(){
        return{
            filterValue: "all"
        }
    },

    methods: {
        test: function(){
            this.$emit("selectDisc",this.filterValue)
        }
    }
}
</script>
