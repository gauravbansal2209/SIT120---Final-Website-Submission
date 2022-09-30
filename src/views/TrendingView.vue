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
        <h2 class="title">Trending Brands</h2>
        <div class="cards">
            <div class="card" v-for="(brand, index) in brands" :key="index">
                <a :href="brand.link" target="_blank">
                    <img :src="require(`@/assets/${brand.logo}`)" alt="">
                </a>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    data(){
        return{
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
            @media only screen and (max-width:1120px){
                padding: 40px 30px;
            }
            .title{
                font-weight: 900;
                font-size: 36px;
                color: #921B95;
                text-align: left;
            }
            .cards{
                display: flex;
                flex-wrap: wrap;
                .card a{
                    height: 150px;
                    margin: 10px;
                    img{
                        height: 150px;
                        box-shadow: 0 0 5px 5px rgba(0, 0, 0, 0.03);
                    }
                }
            }
        }
    }

</style>