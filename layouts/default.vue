<template>
  <div class="container">
    <Navbar />
    <main>
      <nuxt />
    </main>
    <Footer />
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import Footer from "@/components/Footer.vue";
export default {
  components: {
    Navbar,
    Footer
  }
};
</script>

<style lang="less">
//@import url("https://fonts.googleapis.com/css?family=Montserrat&display=swap");

body {
  background-color: rgb(200, 200, 200);
}

.container {
  margin: 0 auto;
  background-color: #fff;
  max-width: 1280px;
  font-size: 14px;
  font-family: "Montserrat", sans-serif;
  color: rgb(255, 255, 255);
  //line-height: 4;
}
</style>
