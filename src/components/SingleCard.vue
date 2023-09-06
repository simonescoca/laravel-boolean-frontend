<template>
    <div class="drink-card">
        <div class="img-wrapper">
            <img :src="cocktail.image" alt="">
        </div>
        <h2>
            <router-link :to="{name: 'cocktail.show', params: {slug:cocktail.slug}}" >
                {{ cocktail.name }}
            </router-link>
        </h2>
    </div>
</template>
<script>

export default {
    name: 'SingleCard',
    props:{
        'cocktail' : Object
    },
}
</script>
<style lang="scss">
    
@use '../styles/partials/variables' as *;

.drink-card{
    background-color: #010514;
    color: white;
    padding: 15px;
    margin: 10px;
    border-radius: 10px;
    width: calc( (100% / 3) - 20px );
    font-family: 'Lora', serif;
    font-style: italic;
    //display: flex;

    img{
        width: 100%;
        object-fit: cover;
        height: 400px;
        justify-content: center;
        border-radius: 10px;
    }

    *{
        margin-bottom: 10px;
    }

    &:hover{
        cursor: pointer;
        background-color: rgba(2, 5, 22, 0.92);
    }

    h2{
        display: block;
        text-align: center;

        a{
            text-decoration: none;
            color: white;
        }
    }

}
</style>