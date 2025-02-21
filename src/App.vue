<template>
  <div id="app">
    <Hero />
    <!-- <main>
      <h2>Welcome to My Vue Project</h2>
      <p>This is a simple test page with a header and footer.</p>
    </main> -->
    <Differences />
    <Items />
    <InfoOne />
    <Slider />

    <InfoTwo />
    <SliderTwo />

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
/* tema 1*/
import InfoOne from "./components/InfoOne.vue";
import Slider from "./components/Slider.vue";

/* tema 2 */
import InfoTwo from "./components/InfoTwo.vue";
import SliderTwo from "./components/SliderTwo.vue";

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
    /* tema 1 */
    InfoOne, 
    Slider,
    /* tema 2 */
    InfoTwo,
    SliderTwo,

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
  user-select: none;
}
</style>
