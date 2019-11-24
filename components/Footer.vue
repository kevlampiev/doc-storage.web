<template>
  <footer>
    <div class="footer__column">
      <h2 class="footer__header">Контактная информация</h2>Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero dolores odit
      repellat.
    </div>
    <div class="footer__column">
      <h2 class="footer__header">Дополнительные материалы</h2>Lorem ipsum dolor sit amet consectetur adipisicing elit. Odio, debitis!
    </div>
    <div class="footer__column">
      <h2 class="footer__header">Версия программы</h2>Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam esse
      eligendi vel consequatur corrupti praesentium.
    </div>
  </footer>
</template>

<style lang="less">
footer {
  min-height: 100px;
  background: url("../assets/wall2.png") repeat;
  background-color: #ccc;
  //filter: opacity(0.5);
  //background-size: 100%;

  color: #222;
  padding: 30px;
  text-align: right;
  font-style: italic;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  clip-path: polygon(0% 0%, 0% 100%, 100% 100%, 100% 15%, 50% 15%, 48% 0%);

  .footer__column {
    width: 30%;
    margin: 15px;
  }

  .footer__header {
    text-transform: uppercase;
    border-bottom: 1px solid #aaa;
    font-style: normal;
    font-size: 14px;
    width: 100%;
    text-align: center;
    color: #999;
  }
}
</style>
