<template>
  <Header title="Portafolio GH" />
  <Container />
  <Footer />
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Container from "./components/Container.vue";

export default{
components:{
  Header,
  Footer,
  Container
},
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}

</style>