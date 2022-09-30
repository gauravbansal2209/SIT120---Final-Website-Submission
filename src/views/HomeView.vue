<template>
    <div class="container">
      <div class="nav">
        <h1 class="logo"><router-link to="/home" tag="a"><span>Shop</span>Cart</router-link></h1>
        <div class="buttons">
          <ul class="items">
            <li><router-link class="item" to="/home">Home</router-link></li>
            <li><router-link class="item" to="/trendingbrands">Trending Brands</router-link></li>
            <li><router-link class="item" to="/contact">Contact</router-link></li>
            <li><router-link class="item" to="/search">Search</router-link></li>
          </ul>
          <button @click="$router.push('/')">sign out</button>
        </div>
      </div>
      <div class="content">
          <!-- Celebrities -->
        <div class="cards-wrapper">
            <h2 class="title">Favourite Celebrity Looks</h2>
            <div class="cards">
                <div class="card" v-for="(celebrity, index) in celebrities" :key="index">
                    <a :href="celebrity.link" target="_blank">
                        <img :src="require(`@/assets/${celebrity.thumbnail}`)" alt="">
                    </a>
                </div>
            </div>
        </div>

          <!-- Brands -->
          <div class="cards-wrapper">
            <h2 class="title">Brands on Top</h2>
            <div class="cards">
            <div class="card" v-for="(brand, index) in brands" :key="index">
                <a :href="brand.link" target="_blank">
                    <img :src="require(`@/assets/${brand.logo}`)" alt="">
                </a>
            </div>
          </div>
          </div>
          <!-- Type of Attire -->
            <div class="cards-wrapper">
                <h2 class="title">Type of Attire</h2>
              <div class="cards">
                  <div class="card" v-for="(attire, index) in attires" :key="index">
                      <a :href="attire.link" target="_blank">
                          <img :src="require(`@/assets/${attire.logo}`)" alt="">
                      </a>
                  </div>
              </div>
            </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
      data(){
          return{
            celebrities:[
                {thumbnail:'brad.jpg', link:'https://en.wikipedia.org/wiki/Brad_Pitt'},
                {thumbnail:'johnny.webp', link:'https://g.co/kgs/wvahtF'},
                {thumbnail:'leon.jpg', link:'http://leonardodicaprio.com/'},
                {thumbnail:'ben.jpg', link:'https://www.imdb.com/name/nm0000255/'},
                {thumbnail:'jeniffer.jpg', link:'https://en.wikipedia.org/wiki/Jennifer_Aniston'},
                {thumbnail:'dawyn.jpg', link:'https://twitter.com/TheRock'},
                {thumbnail:'angelina.jpg', link:'https://en.wikipedia.org/wiki/Angelina_Jolie'},
                {thumbnail:'julia.jpg', link:'https://www.instagram.com/juliaroberts/'},
                {thumbnail:'tom.jpg', link:'http://www.tomcruise.com/'},
            ],
            attires:[
                { logo:'attire1.jpg', link:'https://www.roughguides.com/articles/germany-things-not-to-miss/' },
                { logo:'attire2.jpg', link:'http://www.tripoto.com/travel-guide/armenia' },
                { logo:'attire3.jpeg', link:'https://www.roughguides.com/gallery/traditional-dress/article/the-best-beaches-in-bali/' },
                { logo:'attire4.webp', link:'https://attirethestudio.com/' },
                { logo:'attire5.jpg', link:'https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.whowhatwear.com%2Fcocktail-attire-for-women&psig=AOvVaw0FVdeAVrohN9OIgpDPpotf&ust=1664385666083000&source=images&cd=vfe&ved=0CAwQjRxqFwoTCJidg_O9tfoCFQAAAAAdAAAAABAD' },
                { logo:'attire6.jpg', link:'https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.cosmopolitan.com%2Fstyle-beauty%2Ffashion%2Fa39726192%2Fcocktail-attire-for-women%2F&psig=AOvVaw0FVdeAVrohN9OIgpDPpotf&ust=1664385666083000&source=images&cd=vfe&ved=0CAwQjRxqFwoTCJidg_O9tfoCFQAAAAAdAAAAABAI' },
                { logo:'attire7.jpg', link:'https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.memorandum.com%2F30-dresses-in-30-days%2F10-cocktail-attire-wedding%2F&psig=AOvVaw0FVdeAVrohN9OIgpDPpotf&ust=1664385666083000&source=images&cd=vfe&ved=0CAwQjRxqFwoTCJidg_O9tfoCFQAAAAAdAAAAABAN' },
                { logo:'attire8.jpg', link:'https://www.google.com/url?sa=i&url=https%3A%2F%2Fstylesatlife.com%2Farticles%2Fcocktail-dresses%2F&psig=AOvVaw1j4XL8c8mYruG0mYX7rLAq&ust=1664385793596000&source=images&cd=vfe&ved=0CAwQjRxqFwoTCIDkt66-tfoCFQAAAAAdAAAAABAD' },
                { logo:'attire9.jpg', link:'https://www.google.com/url?sa=i&url=https%3A%2F%2Fstylesatlife.com%2Farticles%2Fcocktail-dresses%2F&psig=AOvVaw1j4XL8c8mYruG0mYX7rLAq&ust=1664385793596000&source=images&cd=vfe&ved=0CAwQjRxqFwoTCIDkt66-tfoCFQAAAAAdAAAAABAN' },
                { logo:'attire10.jpg', link:'https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.promgirl.com%2Fshop%2Fstyles_and_trends%2Fshort-dresses&psig=AOvVaw1j4XL8c8mYruG0mYX7rLAq&ust=1664385793596000&source=images&cd=vfe&ved=0CAwQjRxqFwoTCIDkt66-tfoCFQAAAAAdAAAAABAc' },
          ],
            brands:[
                { logo:'adidas.png', link:'https://www.adidas.com/us' },
                { logo:'amazon.png', link:'https://www.amazon.in/' },
                { logo:'flipkart.png', link:'https://www.flipkart.com/' },
                { logo:'shein.png', link:'https://www.shein.in/' },
                { logo:'armani.png', link:'https://www.armani.com/' },
                { logo:'gucci.png', link:'https://www.gucci.com/' },
                { logo:'myntra.png', link:'https://www.myntra.com/' },
                { logo:'ajio.png', link:'https://www.ajio.com/' },
                { logo:'firstcry.png', link:'https://www.firstcry.com/' },
                
            ]
          }
      }
  
  }
  </script>
  
  <style lang="scss" scoped>
      .container{
          width: 100%;
          .nav{
            width: 100%;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 40px 50px;
            @media only screen and (max-width:1120px){
                padding: 40px 30px;
            }
            @media only screen and (max-width:780px){
                flex-direction: column;
                align-items: flex-start;
            }
            .logo{
                font-weight: 900;
                font-size: 40px;
                @media only screen and (max-width:780px){
                    margin-bottom: 20px;
                }
                a{
                    text-decoration: none;
                    color: #000;
                    span{
                        color: #FC66FF;
                    }
                }
              }
            .buttons{
                display: flex ;
                align-items: center;
                @media only screen and (max-width:780px){
                    flex-direction: column;
                    align-items: flex-start;
                }
                .items{
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    list-style: none;
                    @media only screen and (max-width:780px){
                        margin-bottom: 15px;
                    }
                    @media only screen and (max-width:580px){
                        flex-direction: column;
                        align-items: flex-start;
                    }
                    .item{
                        text-decoration: none;
                        color: #000;
                        margin-right: 15px;
                        @media only screen and (max-width:580px){
                            margin-bottom: 10px;
                        }
                        &:hover{
                        color: #8D188F;
                        }
                    }
                }
                button{
                    width: 87px;
                    height: 42px;
                    background: transparent;
                    border-radius: 8px;
                    border: 1px solid #C15DFF;
                    margin-right: 15px;
                    font-weight: 500;
                    font-size: 18px;
                    color: #000000;
                    text-transform: capitalize;
                    cursor: pointer;
                    &:hover{
                    background: #C15DFF;
                    }
                }
            }
        }
          .content{
              padding: 60px 50px;
              .cards-wrapper{
                margin-bottom: 50px;
                width: 100%;
                  .title{
                      font-weight: 900;
                      font-size: 24px;
                      color: #921B95;
                      text-align: left;
                      margin-bottom: 20px;
                  }
                  .cards{
                    width: 100%;
                      display: flex;
                      flex-wrap: wrap;
                      .card a{
                          img{
                            box-shadow: 0 0 5px 5px rgba(0, 0, 0, 0.03);
                              height: 150px;
                              margin-right: 30px;
                              margin-bottom: 30px;
                          }
                      }
                  }
              }
          }
      }
  
  </style>