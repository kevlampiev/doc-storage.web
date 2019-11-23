<template>
  <div class="editCard-form" v-show="showModal">
    <form action>
      <label for="name">Наименование</label>
      <input type="text" name="name" />
      <label for="description">Краткое описание</label>
      <textarea name="description" id="description" cols="30" rows="10"></textarea>
    </form>
  </div>
</template>

<script>
export default {
  props: ["showModal"]
};
</script>

<style lang="less">
.editCard-form {
  width: 70vw;
  height: 50vh;
  background-color: #fff;
  border: 1px solid #aaa;
  box-shadow: 7px 7px 5px 0px rgba(201, 201, 201, 0.75);
}
</style>