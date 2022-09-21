<template>
  <h1> Hey, This is my component...</h1>
  <h2>  {{name}}  {{greeting}},my hobby is {{hobby}} </h2>
  <h3> {{userName}} is {{rollno}}</h3>
</template>

<script>
export default {
  //props:['greeting','userName','hobby'],
props:{
 rollno:{
  type:Number,
  default:90
 },
 userName:{
  type:String
 },
 hobby:{
  type:String,
  required: true
 }
 },
  data(){
    return {
      name:"Shreyas"
    }
  }

}
</script>

<style>

</style>