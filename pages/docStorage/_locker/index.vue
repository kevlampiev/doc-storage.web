<template>
  <div class="ma">
    <h1>Система хранения. Стеллажи {{$route.params.id}}</h1>

    <div class="controlPanel">
      <Search />
      <button class="addBtn">
        <i class="fa fa-plus-square-o" aria-hidden="true" @click.prevent="addCard()">Добавить</i>
      </button>
    </div>

    <div class="cardsContainer">
      <card v-for="card of cardArray" :key="card.id" :card="card" :cardsSettings="cardsSettings"></card>
    </div>

    <div class="summaryBand">
      Lorem ipsum dolor sit amet consectetur, adipisicing elit. Excepturi,
      reiciendis?
    </div>
    <editCard
      :currentCard="currentCard"
      v-if="stateCode === 1 || stateCode === 2"
      :editFormTitle="stateCode === 1 ? 'Добавление записи' : 'Изменение записи'"
    />
    <deleteConfForm :deleteConfirmation="stateCode === 3" />
  </div>
</template>

<script>
import Card from "../../../components/card";
import deleteConfForm from "../../../components/confirmation";
export default {
  layout: "default",
  data: () => {
    return {
      stateCode: 0, //0 -режим чтения, 1 - добавить, 2- изменить, 3 - удалить запись
      cardsSettings: {
        iconClass: "fa fa-home",
        nextIconClass: "fa fa-tasks",
        url_img: "../../../assets/icons/place.jpg"
      },
      cardArray: [],
      currentCard: {},
      currentIndex: 0
    };
  },
  methods: {
    addCard() {
      this.currentCard = {};
      this.stateCode = 1;
    },

    editCard(card) {
      this.currentIndex = this.cardArray.indexOf(card);
      this.currentCard = Object.assign({}, card);
      this.stateCode = 2;
    },
    deleteCard(card) {
      if (card.ItemsCount === 0) {
        this.currentCard = card;
        this.stateCode = 3;
      }
    },
    /**
     * Завершает модификацию списка карточек
     */
    post() {
      switch (this.stateCode) {
        case 1:
          this.cardArray.push(this.currentCard);
          break;
        case 2:
          this.cardArray[this.currentIndex] = this.currentCard;
          break;
        case 3:
          this.cardArray = this.cardArray.filter(el => el !== this.currentCard);
          break;
      }
      this.stateCode = 0;
    },
    cancel() {
      this.stateCode = 0; //Перешли в режим просмотра и все
    }
  },

  computed: {},
  components: {
    Card,
    editCard: () => import("../../../components/cardEdit"),
    Search: () => import("../../../components/search"),
    deleteConfForm: () => import("@/components/confirmation")
  },
  async mounted() {
    this.cardArray = await this.$axios.$get(
      "https://raw.githubusercontent.com/kevlampiev/JSONdata/master/jsLessonsLvl2/selectAllBuildings.json"
    );
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
