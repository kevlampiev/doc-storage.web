<template>
  <div class="login-div">
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
  layout: "empty"
};
</script>

<style lang="less">
.login-div {
  color: #444;
  border: 1px solid #bbb;
  width: 300px;
  margin: auto;
  padding: 20px;
  box-shadow: 7px 7px 5px 0px rgba(201, 201, 201, 0.75);
  height: 200px;
  form {
    //padding: 25px;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    input {
      width: 258px;
      height: 25px;
      margin: 15px 0;
      border-radius: 12px;
      padding-left: 12px;
      background-color: rgba(255, 166, 0, 0.3);
      border: 1px solid #bbb;
    }
    button {
      height: 25px;
      width: 80px;
      border-radius: 12px;
      background-color: rgba(255, 166, 0, 0.3);
      border: 1px solid #bbb;
    }
    label {
      color: #777;
      width: 258px;
    }
  }
}
</style>