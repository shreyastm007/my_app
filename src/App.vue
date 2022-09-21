<template>

  <h1> Hello Vue</h1>
  <!-- rendering MyComponent-->
  <!-- <my-component greeting="good morning"  :userName="123"
  :rollno=" 10"  :hobby="hobby"/>  -->
  <child-component  @getDataFromChild="getDataFromChild"/>
  <h3> Data of toy from child:{{kidsToyData}}</h3>

</template>

<script>
import ChildComponent from './components/ChildComponent.vue'
// import MyComponent from './components/MyComponent.vue'

export default {
  
  name: 'App',

  components: {
    ChildComponent
    
    //MyComponent
  },

  //data
  data() {
return {
  //userName: "avi",
  hobby:"cricket",
  kidsToyData:""
}
  },

  methods:{
    getDataFromChild(childData){
console.log("chocolate function executed",childData)
this.kidsToyData=childData
    }
  }
}
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
