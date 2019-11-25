<template>
  <div class="editCard-form box-shadowed" v-show="showModal">
    <h2>Изменение информации о месте хранения</h2>
    <button class="close-btn" @click.prevent="closeForm()">X</button>
    <form action>
      <label for="name">Наименование</label>
      <input type="text" name="name" />
      <label for="description">Краткое описание</label>
      <textarea name="description" id="description" cols="30" rows="10"></textarea>
      <button @click.prevent="closeForm()">Сохранить</button>
      <button @click.prevent="closeForm()">Отмена</button>
    </form>
  </div>
</template>

<script>
export default {
  props: ["showModal"],
  methods: {
    closeForm() {
      this.$parent.showModal = false;
    }
  }
};
</script>

<style lang="less">
.editCard-form {
  width: 680px;
  height: 400px;
  background-color: #fff;
  position: fixed;
  top: 100px;
  left: calc(50%-340px);
  form {
    width: calc(100%-22px);
    height: calc(100%-22px);
    border: 1px solid #bbb;
    padding: 10px;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-content: center;
    position: relative;

    input {
      width: 600px;
      margin-bottom: 25px;
    }

    label {
      width: 600px;
    }

    textarea {
      width: 600px;
      height: 150px;
      //margin-bottom: 25px;
    }

    button {
      margin: 25px 10px;
      width: 120px;
    }
  }

  .close-btn {
    position: absolute;
    top: 10px;
    right: 10px;
    width: 25px;
  }
  h2 {
    margin-top: 0;
    width: 100%;
    color: #777 !important;
    background: linear-gradient(
      to bottom,
      #fff,
      #f3f3f3 50%,
      #fff 50%,
      #f3f3f3
    );
    background-size: 100% 10px;
  }
}
</style>