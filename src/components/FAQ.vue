<template>
    <div class="faq-container">
      <h2 class="faq-title">Preguntas Frecuentes</h2>
      <div class="faq-content">
        <div class="faq-image">
          <img src="../assets/otros/pediatra.png" alt="Imagen relacionada" />
        </div>
        <div class="faq-accordion-container">
          <div class="faq-accordion">
            <div v-for="(question, index) in questions" :key="index" class="accordion-item">
              <button class="accordion-header" @click="toggle(index)">
                {{ question.title }}
                <span :class="{'rotate': activeIndex === index}" class="accordion-icon">+</span>
              </button>
              <div v-if="activeIndex === index" class="accordion-body">
                <p>{{ question.content }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        activeIndex: null,
        questions: [
          {
            title: "¿Qué significa que tienen fórmulas avaladas y aprobadas por pediatras?",
            content: "Contenido de prueba 1",
          },
          {
            title: "¿Todos los productos son libres de parabenos, sal, colorantes, sulfatos y cloruro de sodio adicionados?",
            content: "Contenido de prueba 2",
          },
          {
            title: "¿Los productos Arrurrú contienen conservantes?",
            content: "Contenido de prueba 3",
          },
          {
            title: "¿Arrurrú utiliza fragancia en sus productos?",
            content: "Contenido de prueba 4",
          },
          {
            title: "¿Las toallitas de Arrurrú tienen proteína de leche?",
            content: "Contenido de prueba 5",
          },
        ],
      };
    },
    methods: {
      toggle(index) {
        this.activeIndex = this.activeIndex === index ? null : index;
      },
    },
  };
  </script>
  
  <style scoped>
  .faq-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 20px;
  }
  
  .faq-title {
    text-align: center;
    font-size: 24px;
    font-weight: bold;
    margin-bottom: 20px;
  }
  
  .faq-content {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
    width: 100%;
  }
  
  .faq-image img {
    width: 100%;
    height: auto;
    object-fit: cover;
    border-radius: 8px;
  }
  
  .faq-accordion-container {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
  }
  
  .faq-accordion {
    width: 90%;
  }
  
  .accordion-item {
    border: 1px solid #ddd;
    border-radius: 8px;
    margin-bottom: 10px;
    overflow: hidden;
  }
  
  .accordion-header {
    background: #f0f8ff;
    color: #333;
    padding: 15px;
    text-align: left;
    font-size: 16px;
    border: none;
    width: 100%;
    cursor: pointer;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .accordion-body {
    padding: 15px;
    background: #fff;
    font-size: 14px;
  }
  
  .accordion-icon {
    transition: transform 0.3s;
  }
  
  .accordion-icon.rotate {
    transform: rotate(45deg);
  }
  
  /* Responsive Design */
  @media (max-width: 768px) {
    .faq-content {
      grid-template-columns: 1fr;
    }
  }
  </style>
  