<template>
        <div class="jumbotron">
        <h1>
            About US
        </h1>
    </div>
    <section class="about-index">
        <div class="who-we-are">
            <h1>
                Who we are
            </h1>
            <p>
                Welcome to Cocktail Club, where the art of mixology meets unparalleled quality and taste. Founded in 1266 BC, we have quickly become a cornerstone in the world of crafted cocktails, bringing a slice of elegance and a sprinkle of sophistication to bars and homes alike.
                What started as a simple dream to elevate the everyday drink has transformed into a brand that’s synonymous with joy, celebration, and unforgettable moments. Our cocktails are not just beverages; they are an experience—carefully crafted to perfection, made only with the finest ingredients that we source from around the globe.
                Here at Cocktail Club, we believe in innovation and tradition, which is why we’re always exploring new ways to refine and enhance the cocktail experience, while staying true to its classic origins. Whether it’s a romantic date night, a casual get-together, or a grand celebration, our cocktails are designed to make every moment special.
            </p>
        </div>
        <div class="team">
            <h1>The team</h1>
            <div class="team-index">
                <!-- Single Team Card -->
                <div class="team-card" v-for="member in teamMembers">
                    <div class="img-wrapper">
                        <img src="https://www.kindpng.com/picc/m/24-248253_user-profile-default-image-png-clipart-png-download.png" :alt="member">
                    </div>
                    <h2>
                        {{ member }}
                    </h2>
                </div>

            </div>
        </div>
    </section>

</template>
<script>
export default {
    data() {
        return {
            teamMembers: [
                'Simone Scoca',
                'Liza Koizumi',
                'Juan Francisco Markan',
                'Francesco Ruggeri',
                'Mohamed Jebali',
                'Matteo Didone'
            ],
        }
    },
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
  
  .jumbotron{
      background-image: linear-gradient(rgba(200, 151, 151, 0.05), rgba(0, 0, 0, 0.80)), url(https://images.unsplash.com/photo-1597290282695-edc43d0e7129?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2075&q=80);
      width: 100%;
      overflow: hidden;
      height: 300px;
      background-position: 45% 25%;
      position: relative;

      h1{
          font-size: 400;
          color: white;
          position: absolute;
          left: 50%;
          top: 50%;
          transform: translate(-50%, -50%);
          
      }
  }

.about-index{
    background-color: $background-color;
    padding: 50px 60px;
    .who-we-are {
      margin-bottom: 5rem;

        h1{
           color: $text;
        }
        p {
            max-width: 80%;
            margin-left: 4rem;
        }
    }
    .team {
        h1{
           color: $text;
        }
        .team-index {
            margin: 0 auto;
            width: 80%;
            display: flex;
            flex-wrap: wrap;
            .team-card{
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
        }
    }
}

</style>