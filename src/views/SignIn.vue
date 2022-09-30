<template>
  <div class="home">
    <div class="nav">
      <h1 class="logo"><span>Shop</span>Cart</h1>
      <div class="buttons">
        <button >sign up</button>
        <button style = "background-color: #8D188F" @click="$router.push('/')">log in</button>
      </div>
    </div>
    <div class="content">
      <div class="left">
        <h1 class="slogan">ALL BRANDS.<br>ONE PLATFORM.</h1>
      <div class="buttons">
        <button class="acitve">Personal</button>
        <button>Business</button>
      </div>
      </div>
      <div class="right">
        <div class="heading">
          <p class="active">Log In</p>
          <p>Sign up</p>
        </div>
          <p>Username</p>
          <input type="text">
          <p>Password</p>
          <input type="password">
          <p class="forget">Forget password?</p>
          <button class="login" @click="$router.push('/home')">Log In</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeView',
}
</script>
<style lang="scss" scoped> 
.home{
  width: 100%;
  min-height: 100vh;
  background-image: linear-gradient(rgba(141, 24, 143, 0.8),rgba(141, 24, 143, 0.8)), url('@/assets/hero.webp');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;

  .nav{
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 40px 50px;
    @media only screen and (max-width:1120px){
      padding: 40px 30px;
    }
    @media only screen and (max-width:680px){
      align-items: flex-start;
      flex-direction: column;
    }

    .logo{
      font-weight: 900;
      font-size: 40px;
      color: #fff;
      @media only screen and (max-width:680px){
        margin-bottom: 20px;
      }

      span{
        color: #FC66FF;
      }
    }
    .buttons{
      display: flex ;
      align-items: center;
      button{
        width: 87px;
        height: 42px;
        background: transparent;
        border-radius: 8px;
        border: 1px solid #C15DFF;
        margin-right: 15px;
        font-weight: 500;
        font-size: 18px;
        color: #FFFFFF;
        text-transform: capitalize;
        cursor: pointer;
        &:hover{
          background: #C15DFF;
        }
      }
    }

    }
  .content{
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 50px;
    @media only screen and (max-width:1120px){
      flex-direction: column;
      align-items: flex-start;
      padding: 0 30px;
    }
    .left{
      .slogan{
        font-weight: 900;
        font-size: 60px;
        line-height: 80px;
        text-align: left;
        color: #fff;
        @media only screen and (max-width:680px){
          font-size: 40px;
          line-height: 50px;
          margin-bottom: 20px;
        }
      }
      .buttons{
        display: flex;
        button{
          margin-right: 15px;
          background: transparent;
          font-weight: bold;
          font-size: 24px;
          color: #FC66FF;
          border: none;
          border-radius: 8px;
          padding: 10px;
          &:hover{
            background: rgba(131, 13, 204, 0.5);
          }
        }
        .acitve{
          background: rgba(131, 13, 204, 0.5);
        }
      }
    }
    .right{
      display: flex;
      flex-direction: column;
      width: 444px;
      text-align: left;
      @media only screen and (max-width:1120px){
        margin-top: 50px;
        flex-direction: column;
        align-items: flex-start;
      }
      @media only screen and (max-width:680px){
        width: 100%;
      }
      
      p{
        font-size: 18px;
        font-weight: 500;
        margin-bottom: 8px;
        color: #fff;
      }
      input{
        width: 100%;
        height: 50px;
        background: rgba(252, 93, 255, 0.24);
        border-radius: 8px;
        margin-bottom: 30px;
        border: none;
        outline: none;
        padding: 10px;
        font-size: 16px;
        
      }
      .forget{
        text-align: right;
      }
      .login{
        align-self: flex-end;
       width: 80px;
       height: 40px;
       font-size: 18px;
       font-weight: 500;
       border-radius: 8px;
       background: #FC5DFF;
       color: #8D188F;
       border: none;
       cursor: pointer;
      }
      .heading{
        display: flex;
        margin-bottom: 40px;
        p{
          font-size: 26px;
          font-weight: 800;
          margin-right: 20px;
          color: #FC5DFF;
        }
        .active{
          color: #fff;
        }
      }
    }
  }
}

</style>
