<template>
  <div class="delConf-form box-shadowed" v-if="deleteConfirmation">
    <h2>Действительно удалить запись?</h2>
    <button class="close-btn" @click.prevent="$parent.cancel()">X</button>
    <form action>
      <button @click.prevent="$parent.post()">Удалить</button>
      <button @click.prevent="$parent.cancel()">Отмена</button>
    </form>
  </div>
</template>

<script>
export default {
  props: ["deleteConfirmation"],
  methods: {}
};
</script>

<style lang="less">
.delConf-form {
  width: 480px;
  height: 150px;
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