<template>
  <v-app id="inspire">
<div class="justify-center">
  <div class="header">
       
      <h2>Welcome to the Play Ground</h2>

    <h3 class="black">Enter the datas for Levels</h3>
     <v-text-field placeholder="Id (Optional for Add Data)" v-model="identity"></v-text-field>
    <v-text-field placeholder="Name" v-model="name"></v-text-field>
    <v-text-field placeholder="Type" v-model="type"></v-text-field>
    <v-text-field placeholder="Identifier" v-model="identifier"></v-text-field>
    
    <v-btn class="green darken-1 lighten-4 my-2 mx-2">Add Data</v-btn> 
    <v-btn class="blue lighten-4 mx-2 dark">Update Data</v-btn>
    <v-btn class="red lighten-3 lighten-4 my-1 mx-2">Delete Data</v-btn>
    <v-btn class="green lighten-3 lighten-4 mx-2">Find Data</v-btn>
  </div>
  </div>
  </v-app>
</template>

<script>
export default {
    name:"Playground",
    
    data() {
        return{
        levelInput:{identity:"",    
        name:"",
        type:"",
        identifier:"",
        },
    }
     },
    methods:{
        addlevel(){
            this.$store.dispatch("actionLevel",this.levelInput);
        }

    },
   


}
</script>

<style>
.header{
    color: rgb(23, 226, 158);
    border: black;
    border-radius: 20px;
    
    
    padding: 50px;
   
}
</style>