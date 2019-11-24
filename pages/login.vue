<template>
  <div class="login-div box-shadowed">
    <form>
      <label for="login">Логин</label>
      <input type="text" name="login" />
      <label for="password">Пароль</label>
      <input type="password" name="password" />
      <button>Войти</button>
    </form>
  </div>
</template>

<script>
export default {
  layout: "login"
};
</script>

<style lang="less">
.login-div {
  color: #444;
  background-color: #fff;
  width: 300px;
  margin: auto;
  padding: 20px;
  height: 200px;
  filter: opacity(1) brightness(100%);
  form {
    //padding: 25px;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    input {
      width: 258px;
      //      height: 25px;
      margin: 15px 0;
      // border-radius: 12px;
      // padding-left: 12px;
      // background-color: rgba(255, 166, 0, 0.3);
      // border: 1px solid #bbb;
    }
    button {
      //      height: 25px;
      width: 80px;
      // border-radius: 12px;
      // background-color: rgba(255, 166, 0, 0.3);
      // border: 1px solid #bbb;
    }
    label {
      color: #777;
      width: 258px;
    }
  }
}
</style>