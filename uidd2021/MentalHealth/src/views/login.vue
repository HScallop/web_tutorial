<template>
  <div class="login-container">
    <Nav/>
    <div class="login-text">Log In</div>
    <div class="login-img"></div>
    
    <form>
      <div class="form-group">
        <input type="text" class="student-id" placeholder="          請輸入學號" />
        <div class="id-icon"></div>
      </div>
      <div class="form-group">
        <input type="password" class="password" placeholder="          請輸入密碼" />
        <div class="password-icon"></div>
      </div>
      <div class="form-group">
        <button type="submit" class="login-button" @click="signin">登入</button>
      </div>
    </form>
    <span class="forget-password">忘記密碼？</span>

    <p class="no-account"><span>還沒有帳號？</span></p>
    <div class="signup" @click="goto_registration">立即註冊</div>
  </div>
</template>


<script>
export default {
  name: "login",

  methods: {
    signin() {
      this.$router.push("/home");
    },
    goto_registration() {
      this.$router.push("/registration");
    },
  },
};
</script>

<style rel="stylesheet/scss" lang="scss" scoped>
.login-container {
  border: 0;
  padding: 0;
  width: 375px;
  height: 811px;
  .login-text {
    text-align: center;
    line-height: 10.93vw;
    position: absolute;
    width: 25vw;
    height: 15vw;
    left: 38.67vw;
    top: 48.53vw;
    font-family: SF Pro Display;
    font-style: normal;
    font-weight: 600;
    font-size: 8vw;
    display: flex;
    align-items: center;
    color: #1E1E1E;
  }
  .login-img {
    position: absolute;
    width: 61.07vw;
    height: 36.53vw;
    left: 19.47vw;
    top: 66.13vw;
    background-image: url("../assets/svg/login.svg");
    background-repeat: no-repeat;
    background-size: contain;
  }
  form {
    position: absolute;
    top: 113vw;
    left: 12.53vw;
    width: 100vw;
    height: 65.34vw;
    .form-group {
      margin: 0;
      width: 290px;
      height: 50px;
      align-items: center;
      .student-id {
        margin-left: auto;
        margin-right: auto;
        width: 283px;
        height: 42px;
        border-radius: 33px;
        border-width: 1px;
        border-color: #96FBC4;
      }
      .id-icon {
        position: absolute;
        top: 14px;
        left: 18px;
        width: 18px;
        height: 15px;
        background-image: url("../assets/svg/id-icon.svg");
        background-size: contain;
        }
      .password {
        margin-left: auto;
        margin-right: auto;
        width: 283px;
        height: 42px;
        border-radius: 33px;
        border-width: 1px;
        border-color: #20E2D7;
      }
      .password-icon {
        position: absolute;
        top: 60px;
        left: 18px;
        width: 16px;
        height: 17px;
        background-image: url("../assets/svg/password-icon.svg");
        background-size: contain;
        background-repeat: no-repeat;
      }
      .login-button {
        position: absolute;
        height: 42px;
        width: 283px;
        bottom: 25%;
        margin-left: auto;
        margin-right: auto;
        border-radius: 33px;
        border: none;
        background-color: #2DE2D7;
        box-shadow: 0px 4px 17px -1px rgba(107, 182, 177, 0.51);
        font-family: Taipei Sans TC Beta;
        font-weight: 400;
        font-style: normal;
        font-size: 16px;
        color: #FFFFFF;
      }
    }
  }
  .forget-password {
    position: absolute;
    width: 70px;
    height: 17px;
    left: 260px;
    top: 538px;
    font-family: SF Compact Display;
    font-style: normal;
    font-size: 14px;
    font-weight: 400;
    opacity: 0.66;
  }
  p {
    &::after {
      content: '';
      position: absolute;
      display: inline-block;
      width: 281px;
      maring-right: -100%;
      border-bottom: 1px solid #000;
      height: 1px;
      left: 48px;
      top: 636px;
      z-index: -1;
    }
    span {
      color: #5C5C5C;
      background-color: #FFFFFF;
      position: absolute;
      width: 72px;
      height: 16px;
      left: 153px;
      top: 630px;
      font-family: SF Pro Text;
      font-style: normal;
      font-weight: normal;
      font-size: 12px;
      line-height: 16px;
      align-items: center;
    }
  }
  .signup {
    position: absolute;
    height: 43px;
    left: 46px;
    right: 46px;
    top: 691px;
    border: 1px solid #20E2D7;
    box-sizing: border-box;
    border-radius: 33px;
    text-align: center;
    line-height: 43px;
    font-size: 16px;
    color: #8E8E8E;
    font-family: TaipeiSans TC Beta;
    font-weight: 400;
    font-style: normal;
  }
}
  
</style>
