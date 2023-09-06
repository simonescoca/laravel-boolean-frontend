<template>
    <div class="wrapper">
        
        <div class="jumbotron">
            <h1>
                {{ cocktail.name }}
            </h1>
        </div>

        <section class="cocktail-show">
            <img :src="cocktail.image" alt="">
            
            <div class="info">

                <h1>
                    Details
                </h1>

                <div class="ingredients detail-wrapper">
                    <h3>
                        Ingredients
                    </h3>
                    <ul>
                        <li v-for="ingredient in cocktail.ingredients">
                            {{ ingredient.name }}
                        </li>
                    </ul>
                </div>

                <div class="detail-wrapper">
                    <h4>Difficulty Level </h4>
                    <span> {{ cocktail.crafting_difficulty }}/5 </span>
                </div>

                <div class="detail-wrapper">
                    <h4>Making Time </h4>
                    <span> {{ cocktail.crafting_time }} min </span>
                </div>

                <div class="detail-wrapper">
                    <h4>Alcoholic level </h4>
                    <span> {{ cocktail.alcoholic_level }}° </span>
                </div>

                <div class="detail-wrapper">
                    <h4>Type </h4>
                    <span> {{ cocktail.type }} </span>
                </div>

                <div class="detail-wrapper">
                    <h4>Ice </h4>
                    <span v-if="cocktail.with_ice = 1 ? 'Yes' : 'No' "> {{ cocktail.with_ice }} </span>
                </div>

                <div class="detail-wrapper">
                    <h4>Glass Type </h4>
                    <span> {{ cocktail.glass_type }} </span>
                </div>

                <div class="detail-wrapper">
                    <h4>Price </h4>
                    <span> {{ cocktail.price }} &euro;</span>
                </div>

            </div>

        </section>
    </div>
</template>

<script>
import axios from 'axios';
import SingleCard from '../components/SingleCard.vue'

export default {
    name: 'CocktailShow',
    props:{
        'cocktail' : Object
    },

    data() {
        return {
            apiUrl: 'http://127.0.0.1:8000',
            cocktail : false,
        }
    },
    methods: {
        getCocktail(){
            console.log(this.$route.params.slug);
            axios.get(`${this.apiUrl}/api/cocktails/${this.$route.params.slug}`).then((response) => {
                console.log(response);
                this.cocktail = response.data.results;
            }).catch(function (error) {
                console.log(error);
            });
        }
    },
    created(){
        this.getCocktail();
    },
}
</script>


<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@import url('https://fonts.googleapis.com/css2?family=Lora:ital,wght@0,400;0,500;0,600;0,700;1,400;1,500;1,600;1,700&display=swap');

.wrapper{
    background-color: $background-color;
    color: $text;
}
.jumbotron{
    background-image: linear-gradient(rgba(200, 151, 151, 0.05), rgba(0, 0, 0, 0.80)), url(https://images.unsplash.com/photo-1597290282695-edc43d0e7129?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2075&q=80);
    width: 100%;
    overflow: hidden;
    height: 300px;
    background-position: 45% 25%;
    position: relative;

    h1{
        font-family: 'Dancing Script', cursive;
        font-size: 400;
        color: white;
        position: absolute;
        left: 50%;
        top: 50%;
        transform: translate(-50%, -50%);
        
    }
}

.cocktail-show {
    margin: 0 auto;
    width: 100%;
    display: flex;
    height: 100vh;

    img{
        width: 50%;
        height: 100%;
        object-fit: cover;
        filter: grayscale(45%);
    }
    .info{
        font-family: 'Lora', serif;
        width: 50%;
        padding-top: 75px;
        text-align: center;

        h1{
        font-family: 'Lora', serif;
            padding-bottom: 40px;
        }

        .ingredients{
            
            ul{
                list-style-type: none;
            }
        }
    }

    .detail-wrapper{
        margin-bottom: 20px;
    }

}
</style>