
<template>
  <div :key="dog.index" v-for="dog in dogs">
    <h1 class="text-2xl">{{ dog.breed }}</h1>
  </div>
</template>

<script>
// import DisplayBreeds from './DisplayBreeds.vue';
import dogs from '../dogs.js';

export default {
  name: 'App',
  data(){
    return {
      dogs: dogs
    }
  }
}

</script>


