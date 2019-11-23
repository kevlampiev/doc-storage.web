<template>
  <section class="errorNotifitation">
    <h2>Error 404</h2>
    <p>Зaпрашиваемая страница не найдена</p>
    <p>
      Вернуться на
      <nuxt-link to="/">главную</nuxt-link>
    </p>
  </section>
</template>

<script>
export default {};
</script>

<style scoped lang="less">
.cntr {
  margin: 0 auto;
  background-color: #fff;
  max-width: 1280px;
  font-size: 14px;
  font-family: "Montserrat", sans-serif;
  color: #555;

  //line-height: 4;
}

.errorNotifitation {
  color: #444;
  border: 1px solid #444;
  max-width: 500px;
  margin: 20px auto;
  padding: 20px;
  //display: flex;
  //justify-content: center;
  //align-content: center;
  box-shadow: 7px 7px 5px 0px rgba(201, 201, 201, 0.75);
  h2 {
    font-size: 24px;
    color: maroon;
    width: 100%;
    text-align: center;
  }
  p {
    font-size: 20px;
    width: 100%;
    text-align: center;
    //        color: #444;
  }
}
</style>