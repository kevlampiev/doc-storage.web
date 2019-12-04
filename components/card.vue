<template>
  <section v-bind:class="cardsSettings.mainClass">
    <h2 class="card__header">
      <i v-bind:class="cardsSettings.iconClass" aria-hidden="true">&nbsp;&nbsp;{{ card.name }}</i>
    </h2>
    <div
      class="card__description"
      :style="`background: url(${cardsSettings.url_img})`"
    >{{ card.description }}</div>

    <button class="card__editBtn">
      <i class="fa fa-pencil" aria-hidden="true" @click.prevent="$parent.editCard(card)"></i>
    </button>

    <button class="card__deleteBtn" v-if="card.ItemsCount==0">
      <i class="fa fa-trash-o" @click.prevent="$parent.deleteCard(card)" aria-hidden="true"></i>
    </button>
    <button class="card__disabledBtn" v-else>
      <i class="fa fa-trash-o" @click.prevent="$parent.deleteCard(card)" aria-hidden="true"></i>
    </button>

    <button class="card__showItemsBtn" @click="gotoChildren()">
      <i
        v-bind:class="cardsSettings.nextIconClass"
        aria-hidden="true"
      >&nbsp;&nbsp; {{ card.itemsCount }} вложений</i>
    </button>
  </section>
</template>

<script>
export default {
  props: ["card", "cardsSettings"],

  methods: {
    gotoChildren() {
      location.href = `/docStorage/${this.card.id}`;
    }
  },
  computed: {}
};
</script>

<style lang="less">
.card {
  margin: 10px;
  background-color: #f8f8f8;
  width: 200px;
  height: 200px;
  outline: 1px solid #ccc;
  box-shadow: 7px 7px 5px 0px rgba(201, 201, 201, 0.75);
  padding: 5px;

  &__header {
    font-size: medium;
    color: maroon;
    height: 25px;
  }

  &__description {
    height: 110px;
    font-size: smaller;
    font-style: italic;
    overflow: hidden;
    background-color: #fff;
    padding: 5px;
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

  &__disabledBtn {
    font-size: small;
    font-style: italic;
    color: #ccc;
    background-color: #eee;
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

.card-building {
  width: 320px;
  height: 200px;
  background: url("../assets/icons/place.png");
  background-color: rgba(255, 255, 255, 0.95);
  background-blend-mode: color;
  background-size: 100%;
}

.card-locker {
  width: 250px;
  height: 200px;
  background: url("../assets/icons/locker.png");
  background-color: rgba(255, 255, 255, 0.95);
  background-blend-mode: color;
  background-size: 100%;
}

.card-box {
  width: 200px;
  height: 200px;
  background: url("../assets/icons/place.png");
  background-color: rgba(255, 255, 255, 0.911);
  background-blend-mode: color;
  background-size: 100%;
}
</style>
