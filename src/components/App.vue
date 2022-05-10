
<template>
  <div :key="dog.index" v-for="dog in dogs">
    <BreedCard breed="dog.breed" />
  </div>
</template>

<script>
// import DisplayBreeds from './DisplayBreeds.vue';
import dogs from '../dogs.js';
import BreedCard from './BreedCard.vue';

export default {
  name: 'App',
  data(){
    return {
      dogs: dogs
    }
  }
}

</script>


