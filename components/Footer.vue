<template>
  <footer>
    <div class="footer__column">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero dolores odit
      repellat.
    </div>
    <div class="footer__column">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Odio, debitis!
    </div>
    <div class="footer__column">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam esse
      eligendi vel consequatur corrupti praesentium.
    </div>
  </footer>
</template>

<style lang="less">
footer {
  min-height: 100px;
  //background: url('./footer.jpg');
  background-color: rgba(200, 200, 200, 0.6);
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
}
</style>
