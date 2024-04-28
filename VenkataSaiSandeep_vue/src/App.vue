<template>

  <!--Step 3 use the component-->
  <MyHeader storename="My Computer Store" softwername="Windows and IOS" /> 
  <ComputerBox :computers=computers />
 
</template>

<script>
// Step: 1 Import the components
import MyHeader from './components/MyHeader.vue'
import ComputerBox from './components/ComputerBox.vue'


export default{
  name: 'App',

  // Step 2: Register the components
  components:{
    MyHeader,
    ComputerBox
  },
  data(){
    return {
     computers: []
    }
  },
  methods:{
    async fetchcomputers(){
      const res = await fetch('https://sandeep-computerstore-backend.onrender.com/api');
      const data = await res.json()
      console.log(data)
      return data
    }
  },
  async created(){
      this.computers = await this.fetchcomputers();
  }

}
</script>


<style>
body {
  background-image: url(back.jpg);
    height: 100%;
    background-repeat: no-repeat;
    background-attachment: fixed;
    background-size: cover;
    font-family: Arial, Helvetica, sans-serif;
}
</style>
