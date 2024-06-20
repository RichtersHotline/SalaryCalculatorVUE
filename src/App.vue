<template>
  <h1>Calculate your Salary</h1>
<form class="container">
<input type="number" id="workrate" placeholder="enter work rate" v-model="rate">
<input type="number" id="workhours" placeholder="enter hours" v-model="workhrs ">
<label id="salary"></label>
<button @click.prevent="calculateSalary">Calculate Salary</button>
<button @click.prevent="Clearer">Clear</button>





</form>
  

</template>
<script>

export default {
  name: 'App',
  components: {
  },

data() {
 return {
 aster:true,
 rate: "",
 workhrs: ""
 }

 },
 computed: {


 },

 methods: {


  toggleAsterisk() {
   this.aster = !this.aster
 

   
   
  },


  calculateSalary() {

 document.getElementById("salary").innerHTML = "R" + this.rate * this.workhrs


  },
  Clearer() {

    this.rate = ""
    this.workhrs = ""
    document.getElementById("salary").innerHTML = ""
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
.container { 

  display:flex;
  flex-direction:column;
justify-content:center;
width:20%;
margin:auto;
text-align:center;
gap:5px;
}
</style>
