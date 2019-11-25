<template>
  <section class="card">
    <h2 class="card__header">
      <i v-bind:class="iconClass" aria-hidden="true">&nbsp;&nbsp;Место хранения №{{card}}</i>
    </h2>
    <div class="card__description">Pariatur error perferendis maiores explicabo officiis expedita!</div>
    <div class="card__itemsInfo">{{Math.floor(Math.random()*12)}} ящиков</div>
    <button class="card__editBtn">
      <i class="fa fa-pencil" aria-hidden="true" @click.prevent="editCard(card)"></i>
    </button>
    <button class="card__deleteBtn">
      <i class="fa fa-trash-o" @click.prevent="askForDelete()" aria-hidden="true"></i>
    </button>
    <button class="card__showItemsBtn">
      <i v-bind:class="nextIconClass" aria-hidden="true">&nbsp;&nbsp;Содержимое</i>
    </button>
  </section>
</template>

<script>
export default {
  props: ["index", "card", "iconClass", "nextIconClass"],

  methods: {
    editCard(card) {
      //this.$router.push("/docStorage/" + card);
      this.$parent.editCard(card);
    },
    askForDelete() {
      if (!this.$parent.showModal && !this.$parent.deleteConfirmation) {
        this.$parent.deleteConfirmation = true;
      }
    }
  }
};
</script>


<style lang="less">
.card {
  margin: 10px;
  background-color: #f8f8f8;
  // background-image: url("../assets/icons/place.png");
  // opacity: 0.5;
  // background-size: 100%;
  width: 200px;
  height: 200px;
  outline: 1px solid #ccc;
  box-shadow: 7px 7px 5px 0px rgba(201, 201, 201, 0.75);
  padding: 5px;

  &__header {
    font-size: medium;
    color: maroon;
  }

  &__description {
    height: 100px;
    //outline: 1px dashed gray;
    font-size: smaller;
    font-style: italic;
    overflow: hidden;
    background-color: #fff;
  }

  &__itemsInfo {
    height: 20px;
    text-align: right;
    font-size: smaller;
    font-style: italic;
    padding-right: 5px;
  }

  &__editBtn,
  &__deleteBtn {
    font-size: small;
    font-style: italic;
    color: #333;
    background-color: rgba(255, 166, 0, 0.14);
    border: 1px solid #ccc;
    height: 25px;
    border-radius: 12px;
    float: right;
    margin: 5px;
  }

  &__showItemsBtn {
    font-size: small;
    font-style: italic;
    color: #333;
    background-color: rgba(255, 166, 0, 0.14);
    border: 1px solid #ccc;
    height: 25px;
    border-radius: 12px;
    //float: right;
    margin: 5px;
  }

  &__editBtn:hover,
  &__deleteBtn:hover,
  &__showItemsBtn:hover {
    background-color: #222;
    color: blanchedalmond;
  }
}
</style>

