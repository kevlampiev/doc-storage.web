<template>
  <div>
    <h1>Building {{$route.params.id}}</h1>
  </div>
</template>

<script>
export default {
  validate({ params }) {
    console.log("in validate");
    return /^\d+$/.test(params.id);
  }
};
</script>