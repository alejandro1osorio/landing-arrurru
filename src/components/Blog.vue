<template>
  <div class="blog-container">
    <h1>Artículos Recientes</h1>
    <swiper
      :slides-per-view="1"
      :space-between="20"
      :loop="true"
      :breakpoints="{
        768: { slidesPerView: 2 },
        1024: { slidesPerView: 3 }
      }"
      :navigation="true"
      :pagination="{ clickable: true }"
      class="swiper-container"
    >
      <swiper-slide v-for="article in articles" :key="article.id">
        <div class="article">
          <img :src="article.image" alt="Imagen del artículo" class="article-image" />
          <h2>{{ article.title }}</h2>
          <p>{{ article.description }}</p>
          <a :href="article.link" target="_blank" class="view-more">Ver más</a>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";
import { Navigation, Pagination } from "swiper/modules";

export default {
  name: "Blog",
  components: {
    Swiper,
    SwiperSlide
  },
  setup() {
    return {
      modules: [Navigation, Pagination]
    };
  },
  data() {
    return {
      articles: [
        { id: 1, title: "Estructura,función y cuidados de la piel del recién nacido", description: "La línea divisoria entre un proceso patológico y el fisiológico en la piel del recién nacido es confusa. Como consecuencia de ello, la piel del neonato puede presentar una variedad sorprendente de lesiones, algunas inocentes y temporales como resultado de una respuesta fisiológica, o como consecuencia de una enfermedad episódica, y otras, incluso, indicadoras de una enfermedad más grave, que pueden llegar a ser fatales.", image: "https://images.unsplash.com/photo-1740672455853-7ae77b474cbb?q=80&w=2014&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D", link: "https://drive.google.com/file/d/1U_yDhoc2ufu2BHXQUK_pdEUpYZy4U_AF/view?usp=sharing" },
        { id: 2, title: "Guía Del Cuidado", description: "La piel del ser humano consta de tres capas: la epidermis, la dermis y el tejido celular subcutáneo, que derivan embriológicamente del ectodermo (la primera) y del mesodermo (las dos últimas). En el neonato a término (que es aquél que nace entre las semanas 37 y 41 de embarazo), la epidermis, los anexos cutáneos y la unión dermoepidérmica están completamente formados, pero todavía presentan algunos rasgos propios de su inmadurez: la red de crestas interpapilares está menos desarrollada que en el adulto y la cohesión dermoepidérmica es más débil y vulnerable a los pequeños traumatismos.", image: "https://images.unsplash.com/photo-1740672535321-8857a3e79039?q=80&w=1962&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D", link: "https://drive.google.com/file/d/1m0P42YEyIKBWIwB-v-KDWEaCfk-iaiDl/view?usp=sharing" },
        { id: 3, title: "Newborn infant skin gene expression: Remarkable differences versus adults", description: "Newborn infant skin is truly remarkable, characterized by its notable softness, smoothness and uniformity, yet poised to survive in harsh, hostile conditions following birth [1]. An understanding of this pristine infant skin is key to the maintenance of health, optimum response to insults and restoration of barrier damage and avoidance of disease, e.g., atopic dermatitis. In contrast, adult skin reflects the accumulation of years of assault from its environment, including ultraviolet radiation [2], endogenous aging, changes in temperature and humidity, exposure to irritants [3] and disease, to name a few. Exploration and understanding of the biological processes in newborn skin is a critical factor in mitigating these negative outcomes.", image: "https://images.unsplash.com/photo-1740672540738-99c087d3ca59?q=80&w=2038&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D", link: "https://drive.google.com/file/d/14OiixavGWH1ZFZeq5tnESy3Y5a7maMEE/view?usp=sharing" },
        { id: 4, title: "Newborn Infant Skin: Physiology, Development, and Care", description: "Infant skin is critical to the newborn child’s transition from the womb environment to the journey to self-sufficiency. This review provides an integrative perspective on the skin development in full term and premature infants. There is a particular focus on the role of vernix caseosa and on the implications of skin development for epidermal penetration of exogenous compounds. Healthy full-term newborn skin is well-developed and functional at birth, with a thick epidermis and well-formed stratum corneum (SC) layers.", image: "https://images.unsplash.com/photo-1740672543483-8363b5777471?q=80&w=2059&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D", link: "https://drive.google.com/file/d/1okxiVc2iUHM74NBtEqodVIYcZTAneuja/view?usp=sharing" },
      ]
    };
  }
};
</script>

<style scoped>
.blog-container {
  text-align: center;
  padding: 20px;
}

h1 {
  font-size: 2.5em;
  color: #2c3e50;
  margin-bottom: 30px;
}

.swiper-container {
  width: 100%;
  padding: 20px 0;
}

.article {
  background-color: #f9f9f9;
  border-radius: 8px;
  padding: 15px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  text-align: center;
  overflow: hidden;
}

.article-image {
  width: 100%;
  height: auto;
  border-radius: 8px;
}

h2 {
  font-size: 1.5em;
  margin: 10px 0;
  color: #34495e;
}

p {
  font-size: 1em;
  color: #7f8c8d;
  margin: 10px 20px;
  text-align: justify;
}

.view-more {
  text-decoration: none;
  color: #3498db;
  font-weight: bold;
  transition: color 0.3s;
}

.view-more:hover {
  color: #1d6fa5;
}
</style>
