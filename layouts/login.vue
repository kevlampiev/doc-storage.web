<template>
  <div class="container-login">
    <img src="../assets/logo3.png" alt="Логотип" class="logo_img" />
    <nuxt />
  </div>
</template>

<style lang="less">
body {
  background-color: #ccc;
}
.container-login {
  margin: 0 auto;
  background: url("../assets/wall2.png") repeat;
  max-width: 1280px;
  font-size: 14px;
  font-family: "Montserrat", sans-serif;
  color: #555;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-content: center;
  position: relative;
}

.logo_img {
  position: absolute;
  top: 10px;
  left: 10px;
  width: 400px;
  filter: hue-rotate(25deg) grayscale(50%);
}
</style>