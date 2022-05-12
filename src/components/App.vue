
<template>
  <h1 :class="titleStyle">Doggies 101</h1>
  <div :class="containerStyle">
    <div :class="cardStyle" :key="dog.index" v-for="dog in dogs">
      <BreedCard :breed="dog.breed" :photo="dog.photo" :isHypoallergenic="determineHypoallergy(dog.isHypoallergenic)" :attribution="dog.attribution" />
    </div>
  </div>
</template>

<script>
// import DisplayBreeds from './DisplayBreeds.vue';
import dogs from '../dogs.js';
import BreedCard from './BreedCard.vue';

export default {
    name: "App",
    data() {
        return {
            titleStyle: "bg-blue-700 font-bold py-3 text-3xl text-center text-white",
            dogs: dogs,
            containerStyle: "bg-yellow-100 grid md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-6 justify-items-center p-3",
            cardStyle: "bg-green-300 xl:col-span-2 grid h-auto w-64 xl:w-5/6 justify-items-center my-3 p-3 rounded-xl shadow-xl",
        };
    },
    methods: {
      determineHypoallergy(isHypoallergenic) {
        if (isHypoallergenic) {
          return "Yes";
        } else {
          return "No";
        }
      }
    },  
    components: { BreedCard }
}

</script>


