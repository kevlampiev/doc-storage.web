<template>
  <div class="ma">
    <h1>Система хранения</h1>
    <div class="controlPanel">
      <div class="searchForm">
        <input class="searchForm__input" type="search" placeholder="Enter search string here..." />
        <button class="searchForm__button">
          <!-- <fas icon="search" /> -->
          <!-- <i class="fa fa-search" aria-hidden="true"></i> -->
        </button>
      </div>
      <button class="addBtn">
        <!-- <fa icon="dollar-sign" style="font-size: 12px" /> -->
        <i class="fa fa-plus-square-o" aria-hidden="true">Добавить</i>
      </button>
    </div>

    <div class="cardsContainer">
      <card v-for="(card, index) of 14" :key="index"></card>
    </div>

    <div class="summaryBand">
      Lorem ipsum dolor sit amet consectetur, adipisicing elit. Excepturi,
      reiciendis?
    </div>
  </div>
</template>

<script>
import Card from "../../components/card";
export default {
  methods: {
    editCard(card) {
      this.$router.push("/buildings/" + card);
    }
  },
  components: {
    Card
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

// .card {
//   margin: 10px;
//   background-color: #f8f8f8;
//   width: 200px;
//   height: 200px;
//   outline: 1px solid #ccc;
//   box-shadow: 7px 7px 5px 0px rgba(201, 201, 201, 0.75);
//   padding: 5px;

//   &__header {
//     font-size: medium;
//     color: maroon;
//   }

//   &__description {
//     height: 100px;
//     //outline: 1px dashed gray;
//     font-size: smaller;
//     font-style: italic;
//     overflow: hidden;
//     background-color: #fff;
//   }

//   &__itemsInfo {
//     height: 20px;
//     text-align: right;
//     font-size: smaller;
//     font-style: italic;
//     padding-right: 5px;
//   }

//   &__editBtn,
//   &__deleteBtn {
//     font-size: small;
//     font-style: italic;
//     color: #333;
//     background-color: rgba(255, 166, 0, 0.14);
//     border: 1px solid #ccc;
//     height: 25px;
//     border-radius: 12px;
//     float: right;
//     margin: 5px;
//   }

//   &__showItemsBtn {
//     font-size: small;
//     font-style: italic;
//     color: #333;
//     background-color: rgba(255, 166, 0, 0.14);
//     border: 1px solid #ccc;
//     height: 25px;
//     border-radius: 12px;
//     //float: right;
//     margin: 5px;
//   }

//   &__editBtn:hover,
//   &__deleteBtn:hover,
//   &__showItemsBtn:hover {
//     background-color: #222;
//     color: blanchedalmond;
//   }
// }

.searchForm {
  margin-top: 5px;
  position: relative;
  width: 200px;
  background-color: rgba(255, 166, 0, 0.14);

  &__input {
    width: 100%;
    border: 1px solid #eee;
    border-radius: 5px;
    margin-right: 0;
    padding-right: 0;
    font-size: 14px;
    font-style: italic;
    padding-left: 20px;
    background-color: inherit;
  }

  &__button {
    position: absolute;
    top: 3px;
    left: 3px;
    padding-left: 0;
    background-color: rgba(255, 166, 0, 0.14);
    color: gray;
    border: none;
    border-radius: 5px;
  }
}

.addBtn {
  background-color: rgba(255, 166, 0, 0.3);
  border: 1px solid #ccc;
  height: 25px;
  border-radius: 10px;
  margin-top: 0px;
}

.addBtn:hover {
  background-color: #222;
  color: blanchedalmond;
}

.summaryBand {
  min-height: 30px;
  border-top: 2px solid #ddd;
  //  background-color: blue;
  text-align: right;
  font-style: italic;
  //  clip-path: polygon(0% 0%, 0% 100%, 100% 100%, 100% 25%, 52% 25%, 48% 0%);
}
</style>
