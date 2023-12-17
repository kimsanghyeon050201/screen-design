<template>
  <body>
    <div class="login-wrapper">
        <h2>Login</h2>
        <form method="post" action="서버의url" id="login-form">
            <input type="text" name="userName" placeholder="Email">
            <input type="password" name="userPassword" placeholder="Password">
            <input type="submit" value="Login">
            <span>로그인 이력이 있으신가요? </span>
            <a href="">아니요</a>
        </form>
    </div>
</body>
</template>

<style>
* {
  padding: 0;
  margin: 0;
  border: none;
  /* background: #fff; */
}
body {
  font-size: 14px;
  font-family: "Roboto", sans-serif;
  
}
.login-wrapper {
  width: 400px;
  height: 350px;
  padding: 40px;
  box-sizing: border-box;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.login-wrapper > h2 {
  font-size: 24px;
  color: #0040ff;
  margin-bottom: 20px;
}
#login-form > input {
  width: 100%;
  height: 48px;
  padding: 0 10px;
  box-sizing: border-box;
  margin-bottom: 16px;
  border-radius: 6px;
  background-color: #f8f8f8;
  border: 1px solid;
}
#login-form > input::placeholder {
  color: #d2d2d2;
}
#login-form > input[type="submit"] {
  color: #fff;
  font-size: 16px;
  background-color: #0040ff;
  margin-top: 20px;
}
</style>