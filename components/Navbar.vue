<template>
  <header>
    <div class="header__title">
      <img src="@/assets/logo3.png" alt="Placeholder logo" />
    </div>
    <div class="header__menudiv">
      <ul class="menu">
        <li class="menu__item">
          <nuxt-link exact active-class="active" to="/">Главная</nuxt-link>
        </li>

        <li class="menu__item">
          <nuxt-link active-class="active" to="/docStorage">Хранение</nuxt-link>
        </li>

        <li class="menu__item">
          <a href="#">Календарь</a>
        </li>
        <li class="menu__item">
          <a href="#">Выйти</a>
        </li>
      </ul>
      <div class="userInfo">
        <img src="@/assets/face1.jpg" alt class="userInfo__photo" />
        <p class="userInfo__userName">Имя пользователя</p>
      </div>
    </div>

    <div class="breadCrumbs">
      <a href="#" class="breadCrumbs__link">Система хранения ></a>
      <a href="#" class="breadCrumbs__link">Дом ></a>
      <a href="#" class="breadCrumbs__link">Шкаф в коридоре ></a>
      <a href="#" class="breadCrumbs__link">Коробка №17</a>
    </div>
  </header>
</template>

<style lang="less">
header {
  //width: calc(100%-150px);
  min-height: 75px;
  //background: url("./header.jpg");
  background-color: rgba(200, 200, 200, 0.6);
  background-size: cover;
  color: #777;
  clip-path: polygon(0% 0%, 0% 88%, 48% 88%, 50% 100%, 100% 100%, 100% 0%);
  border-bottom: 1px solid rgb(213, 213, 248);
  padding: 25px 75px;
  position: relative;
  display: flex;
  justify-content: space-between;

  .header__title img {
    width: 200px;
    //opacity: 0.5;
    filter: hue-rotate(25deg);
  }

  .header__menudiv {
    padding: 0;
    margin: 0;
    display: flex;
    justify-content: space-between;
  }
}

.menu {
  //padding: 15px;
  height: 30px;
  display: flex;
  justify-content: right;
}

.menu__item {
  display: block;
  text-decoration: none;
  list-style-type: none;
  margin: 10px;
  height: 25px;

  a {
    display: block;
    font-family: "Montserrat", sans-serif;
    height: 20px;
    font-size: 20px;
    color: #600000;
    font-weight: 700;
    text-decoration: none;
  }

  a:hover {
    color: black;
    font-weight: 600;
    border-bottom: 2px solid black;
    //background-color: #999;
  }
}

.active {
  color: rgb(160, 3, 3) !important;
  border-bottom: 2px solid maroon;
}

.userInfo {
  max-width: 70px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;

  &__photo {
    width: 50px;
    height: 50px;
    border-radius: 25px;
  }

  &__userName {
    width: 100%;
    text-align: center;
  }
}

.breadCrumbs {
  position: absolute;
  bottom: 5px;
  left: 51%;
  color: rgb(92, 3, 37);
  //background-color: #fff;
  //opacity: 0.7;
  font-style: italic;

  .breadCrumbs__link {
    display: inline-block;
    font-family: "Montserrat", sans-serif;
    height: 20px;
    color: maroon;
    text-decoration: none;
    font-weight: 400;
    border-bottom: 1px solid rgba(0, 0, 0, 0.013);
  }

  .breadCrumbs__link:hover {
    color: black;
    font-weight: 500;
    border-bottom: 1px solid black;
    //background-color: #999;
  }
}
</style>
