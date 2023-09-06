<template>
    <div class="jumbotron">
        <h1>
            Welcome to the Cocktail Club
        </h1>
    </div>
    <section class="cocktails-index">
        <h1>
            Our Cocktails
        </h1>
        <div class="cocktails">
            <SingleCard class="cocktail-card" v-for="cocktail in cocktails" :cocktail='cocktail'  />
        </div>
    </section>
</template>
<script>
import axios from 'axios';
import SingleCard from '../components/SingleCard.vue';

export default {
    name: 'Homepage',
    components:{
        SingleCard
    },
    data() {
        return {
            cocktails: [],
            apiUrl: 'http://127.0.0.1:8000/api/cocktails',
        };
    },

    methods: {
        getCocktails() {
            const params = {}
            // console.log(params);
            axios.get(this.apiUrl, { params })
                .then((response) => {
                console.log(response.data.results.data);
                this.cocktails = response.data.results.data;
            })
                .catch(function (error) {
                console.log(error);
            })
                .finally(function () {
            });
        }
    },
    created() {
        this.getCocktails();
    } 
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
  
        .jumbotron{
            background-image: linear-gradient(rgba(200, 151, 151, 0.05), rgba(0, 0, 0, 0.80)), url(https://images.unsplash.com/photo-1597290282695-edc43d0e7129?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2075&q=80);
            width: 100%;
            overflow: hidden;
            height: 650px;
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

        .cocktails-index{
            background-color: $background-color;
            padding-bottom: 70px;

            h1{
                color: $text;
                font-family: 'Dancing Script', cursive;
                padding: 50px 60px;

            }

            .cocktails{
                margin: 0 auto;
                width: 80%;
                display: flex;
                flex-wrap: wrap;
            }
        }
</style>