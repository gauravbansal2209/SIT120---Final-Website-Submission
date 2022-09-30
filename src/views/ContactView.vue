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
        <div class="contactInfo">
            <div class="item">
                <h3 class="title">Contact Info</h3>
                <p class="value">+61 - 491877665</p>
            </div>
            <div class="item">
                <h3 class="title">Email</h3>
                <p class="value">shopcart@gmail.com</p>
            </div>
            <div class="item">
                <h3 class="title">Opening Hours</h3>
                <p class="value">9:00 A.M. to 5:00 P.M.</p>
            </div>
        </div>
        <div class="sendEnquiry">
            <h3 class="title">Send us your Enquiry</h3>
            <input type="text">
        </div>

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
          background: #E5E5E5;
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
              position: relative;
              padding: 120px 50px;
              min-height: 80vh;
              display: flex;
              align-items: flex-start;
              justify-content: center;

              .contactInfo{
                display: flex;
                align-items: center;
                justify-content: center;
                @media only screen and (max-width:980px){
                    flex-direction: column;
                }
                .item{
                    text-align: center;
                    margin-right: 40px;
                    @media only screen and (max-width:980px){
                        margin-right: 0px;
                        margin-bottom: 30px;
                    }
                    .title{
                        font-weight: 700;
                        font-size: 28px;
                        color: #8D188F;
                        margin-bottom: 16px;
                    }
                    .value{
                        font-weight: 500;
                        font-size: 28px;
                        color: #FA00FF;
                    }

                }
              }
              .sendEnquiry{
                position: absolute;
                bottom: 20px;
                text-align: center;
                width: 100%;
                .title{
                    font-weight: 700;
                    font-size: 20px;
                    color: #C15DFF;
                    margin-bottom: 16px;
                }
                input{
                    width: 503px;
                    height: 52px;
                    border: 2px solid #8482F6;
                    border-radius: 8px;
                    background: transparent;
                    font-size: 18px;
                    @media only screen and (max-width:780px){
                        width: 80%;
                    }
                }
              }
          }

      }
  
  </style>