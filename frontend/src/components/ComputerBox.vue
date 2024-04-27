<template>
   <div class="home">
    <div v-for="computer of computers" :key="computer.modelnumber" class="items">
            <h3> {{computer.brand}}</h3>
            <h3> {{computer.modelname}}</h3>
            <h4> {{computer.modelnumber}}</h4>
            <h4> {{computer.storagecapacity}}</h4>
            <h4> {{computer.price}}</h4>
            <h4><a v-bind:href="computer.url" target="_blank">{{computer.url}}</a></h4>
    </div>
 </div>
</template>
<script>
export default {
    name: 'ComputerBox',
    props:{
        computers: Array
    }
    
}
</script>
<style>
h4{
    margin: 5px;
}
h3{
    margin: 5px;
}
.home {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(333px, 2fr));
      grid-gap: 20px;
      padding:20px;
}
.items {
    text-align: center;
    background-color:rgb(255, 255, 255,0.7);
    border-radius: 5px;
    padding: 5px;
    box-shadow: 0 0 20px rgba(0, 0, 0, 1);
}
</style>
