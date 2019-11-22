<template>
  <div class="searchForm">
    <input class="searchForm__input" type="search" placeholder="Enter search string here..." />
    <button class="searchForm__button">
      <!-- <fas icon="search" /> -->
      <i class="fa fa-search" aria-hidden="true"></i>
    </button>
  </div>
</template>
<script>
export default {};
</script>
<style lang="less">
.searchForm {
  margin-top: 5px;
  position: relative;
  width: 200px;
  height: 20px;
  background-color: inherit;

  &__input {
    width: 100%;
    border: 1px solid #eee;
    border-top-right-radius: 10px;
    border-bottom-right-radius: 10px;
    margin-right: 0;
    padding-right: 0;
    font-size: 14px;
    font-style: italic;
    padding-left: 20px;
    background-color: rgba(255, 166, 0, 0.3);
  }

  &__button {
    position: absolute;
    top: 3px;
    left: 3px;
    padding-left: 0;
    background-color: rgba(255, 166, 0, 0.3);
    color: gray;
    border: none;
    border-top-left-radius: 10px;
    border-bottom-left-radius: 10px;
  }
}
</style>