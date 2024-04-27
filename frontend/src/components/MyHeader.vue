<template>
<div class="header">
    <h1> {{storename}} </h1>
    <h2> {{softwername}} </h2>
</div>
</template>

<script>

  export default{
    name: 'MyHeader',
    props:{
        softwername:String,
        storename:String
    }
  }

</script>

<style>
  .header {
    color: black;
    text-align: center;
    padding: 5px;
  }
  h2{
     font-family: Verdana, Geneva, Tahoma, sans-serif;
    font-size: 25px;
    margin: 10px;
  }
  h1{
     font-family: Georgia, 'Times New Roman', Times, serif;
    font-size: 45px;
    margin: 10px;
  }
</style>