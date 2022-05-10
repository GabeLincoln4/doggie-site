<template>
    <div class="bg-yellow-100">
        
        <!-- <h1 :class="pageTitle">Doggies 101</h1>
        <div :class="containerStyle">
            <div :class="cardStyle" v-for="statement in statements">
                <img :class="imageStyle" :src="statement.photo" />
                <div :class="textStyle">
                    <h1 :class="breedStyle">{{ statement.breed }}</h1>
                    <div :class="hypoallergenicStyle">
                        <p>Hypoallergenic?</p>
                        <p :class="nameStyle">{{ statement.isHypoallergenic }}</p>
                    </div>
                </div>
            </div>
        </div> -->
        <!--<h1 v-for="quote in quotes" >{{ quote.quote }}</h1>-->
    </div>
</template>

<script>
    export default {
        name: 'BreedCard',
        data() {
            return {
                pageTitle: "bg-blue-700 font-bold p-2 text-4xl text-center text-white",
                imageStyle: "h-48 object-cover rounded-full w-48",
                containerStyle: "grid md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-6 justify-items-center p-3",
                cardStyle: "bg-green-300 xl:col-span-2 grid h-auto w-64 xl:w-5/6 justify-items-center my-3 p-3 rounded-xl shadow-xl",
                textStyle: "bg-blue-700 font-bold font-serif grid italic place-content-center my-2 text-center text-white  p-2 m-1 rounded-xl w-3/4",
                hypoallergenicStyle: "not-italic font-sans",
                breedStyle: "text-xl mb-3"
            }
        }
    }
</script>