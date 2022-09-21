<template>
  <h1> I am child component</h1>
  <button @click="handleClick"> send data to parent</button>
</template>

<script>
export default {
    emits:["getDataFromChild"],
data() {
    return {
        toyInfo:" this a blue car"
    }
},

methods:{
    
    handleClick(){
        //console.log("")
        this.$emit("getDataFromChild",this.toyInfo)
    }
}
}
</script>

<style>

</style>