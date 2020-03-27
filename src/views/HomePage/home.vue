<template>
  <div>
    <Header/>
    <Carousel/>
    <NewsBox/>
    <Footer/>
  </div>
</template>

<script>
  import Header from "./Header";
  import Carousel from "./Carousel";
  import NewsBox from "./NewsBox";
  import Footer from "./Footer";

  export default {
    components: {
      Header,
      Carousel,
      NewsBox,
      Footer
    }
  }
</script>

<style scoped>

</style>
