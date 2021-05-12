<template>
  <div id="login-container">
    <h1>TEST</h1>
    <div id="navbar">
    </div>
    <div id="login">
      <div id="login-img-container">
        <div id="login-title">Log In</div>
        <div id="login-img"></div>
      </div>
      <div id="login-form-container">
        <input class="input" 
        id="login-id" 
        autocomplete="off" 
        type="text" 
        v-model="formLogin.userName" 
        placeholder="請輸入學號" 
        required>
        <input class="input" 
        id="login-password" 
        autocomplete="off" 
        type="password" 
        v-model="formLogin.userPassword" 
        maxlength="20" 
        @keyup.enter="login" 
        placeholder="請輸入登錄密碼">
      </div>
      <button id="loging-btn" 
        type="primary" 
        :disable="isDisabled" 
        :loading="isLoading" 
        @click.stop="login">登入
      </button>
      <div id="err">
        <p>{{ errorMeg }}</p>
      </div>
      <div id="option">
        <span id="forget-password" href="javascript:;">忘記密碼？</span>
      </div>
    </div>
    <div id="signup">
      <p class="no-account"><span>還沒有帳號？</span></p>
      <a href="" @click="registration">立即註冊</a>
    </div>
  </div>
</template>

<script>
export default {
  };
</script>

<style rel="stylesheet/scss" lang="scss" scoped>
#login-container {
  border: 0;
  padding: 0;
  width: 100vw;
  height: 100vh;
  }
</style>
