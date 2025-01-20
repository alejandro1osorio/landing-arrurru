<template>
  <div id="app">
    <Header />
    <main>
      <h2>Welcome to My Vue Project</h2>
      <p>This is a simple test page with a header and footer.</p>
    </main>
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Footer,
  },
};
</script>

<style>
body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
