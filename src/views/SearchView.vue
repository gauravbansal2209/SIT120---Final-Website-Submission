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
          <form action="http://google.com/search" target="_blank">
              <input type="text" name="q" placeholder="Search">
          </form>
      </div>
    </div>
  </template>
  
  <script>
  export default { 
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
              width: 100%;
              input[type='text']{
                width: 655px;
                height: 70px;
                padding: 10px;
                font-size: 18px;
                border: 2px solid #8D188F;
                border-radius: 8px;
                @media only screen and (max-width:780px){
                    width: 80%;
                }
              }
          }
      }
  
  </style>