<template>

  <section>
      <img src="../assets/gestion_proyectos.png" alt="gestion" >
      <h1>Dog-Management</h1>
     <DogList></DogList>
     <AddDog></AddDog> 
     
  </section>
</template>

<script>


import DogList from './DogTable.vue';
import AddDog from './AddDog.vue';



export default {
    name:'DogManagement',
    components: {
        AddDog,
        DogList
    },

   data: function(){
    return {
      
      tabDog: [{
        id, name, race, birthdate
      }]
      
    }
  },
  methods: {
     
      addDog (){
      tabDog.push();
      },
 
    deleteDog (id){
        this.tabDog.filter(id);
    }
  }
  
}
</script>

<style>

</style>
