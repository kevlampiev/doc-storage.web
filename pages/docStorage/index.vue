<template>
  <div class="ma">
    <h1>Система хранения</h1>
    <div class="controlPanel">
      <Search />
      <button class="addBtn">
        <!-- <fa icon="dollar-sign" style="font-size: 12px" /> -->
        <i class="fa fa-plus-square-o" aria-hidden="true">Добавить</i>
      </button>
    </div>

    <div class="cardsContainer">
      <card v-for="(card, index) of 14" :key="index" :card="card"></card>
    </div>

    <div class="summaryBand">
      Lorem ipsum dolor sit amet consectetur, adipisicing elit. Excepturi,
      reiciendis?
    </div>
  </div>
</template>

<script>
import Card from "../../components/card";
import Search from "../../components/search";
export default {
  methods: {
    editCard(card) {
      this.$router.push("/buildings/" + card);
    }
  },
  components: {
    Card,
    Search
  }
};
</script>

<style lang="less">
.ma {
  color: #333;
  padding: 25px 75px;
}
h1 {
  width: 100%;
  color: #777 !important;
  background: linear-gradient(to bottom, #fff, #f3f3f3 50%, #fff 50%, #f3f3f3);
  background-size: 100% 10px;
}

.controlPanel {
  width: 100%;
  height: 30px;
  color: orangered;
  background-color: #f9f9f9;
  //outline: 1px dashed gray;
  border-bottom: 2px solid #ddd;
  display: flex;
  flex-wrap: nowrap;
  justify-content: space-between;
}

.cardsContainer {
  display: flex;
  flex-wrap: wrap;
  padding: 10px;
  //justify-content: space-between;
}

.addBtn {
  background-color: rgba(255, 166, 0, 0.3);
  border: 1px solid #ccc;
  height: 20px;
  border-radius: 10px;
  margin-top: 5px;
}

.addBtn:hover {
  background-color: #222;
  color: blanchedalmond;
}

.summaryBand {
  min-height: 30px;
  border-top: 2px solid #ddd;
  text-align: right;
  font-style: italic;
}
</style>
