<template>
    
        <img :class="imageStyle" :src="photo" />
        <div :class="textStyle">
            <h1 :class="breedStyle">{{ breed }}</h1>
            <div :class="hypoallergenicStyle">
                <p>Hypoallergenic?</p>
                <p :class="nameStyle">{{ isHypoallergenic }}</p>
            </div>
            <div :class="attributionStyle">- {{ attribution }}</div>
        </div>
     
        <!--<h1 v-for="quote in quotes" >{{ quote.quote }}</h1>-->

</template>

<script>
    export default {
        props: ['breed', 'photo', 'isHypoallergenic', 'attribution'],
        name: 'BreedCard',
        data() {
            return {
                pageTitle: "bg-blue-700 font-bold p-2 text-4xl text-center text-white",
                imageStyle: "h-48 object-cover rounded-full w-48",
                textStyle: "bg-blue-700 font-bold font-serif grid grid-cols-2 italic place-content-center my-2 text-center text-white  p-2 m-1 rounded-xl w-3/4",
                hypoallergenicStyle: "col-span-2 not-italic font-sans",
                breedStyle: "text-xl mb-3 col-span-2",
                attributionStyle: "col-start-2 mt-2 place-self-end text-right text-tiny"
            }
        }
    }
</script>