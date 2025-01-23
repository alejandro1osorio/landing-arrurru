<template>
  <div id="app">
    <Hero />
    <!-- <main>
      <h2>Welcome to My Vue Project</h2>
      <p>This is a simple test page with a header and footer.</p>
    </main> -->
    <Differences />
    <Items />
    <Benefits />
    <Blog />
    <FAQ />
    <Footer />
  </div>
</template>

<script>
import Hero from "./components/Hero.vue";
import Differences from "./components/Differences.vue";
import Items from "./components/Items.vue";
import Benefits from "./components/Benefits.vue";
import Blog from "./components/Blog.vue"
import FAQ from "./components/FAQ.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Hero,
    Differences,
    Items,
    Benefits,
    Blog,
    FAQ,
    Footer,
  },
};
</script>

<style>
body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  background-color: #F3F3F3;
}
</style>
