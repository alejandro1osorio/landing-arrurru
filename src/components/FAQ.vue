<template>
    <div class="faq-container">
      <h2 class="faq-title">
        Preguntas <span class="highlight">Frecuentes</span>
      </h2>
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
      <div class="bottom-line"></div>
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
            content: "Nuestras fórmulas han sido evaluadas por expertos pediatras, garantizando seguridad y calidad para el cuidado de tu bebé.",
          },
          {
            title: "¿Todos los productos son libres de parabenos, sal, colorantes, sulfatos y cloruro de sodio adicionados?",
            content: "Sí, nuestros productos están diseñados sin ingredientes agresivos, cuidando la piel sensible de los bebés.",
          },
          {
            title: "¿Los productos Arrurrú contienen conservantes?",
            content: "Utilizamos conservantes aprobados para mantener la frescura de nuestros productos sin comprometer su seguridad.",
          },
          {
            title: "¿Arrurrú utiliza fragancia en sus productos?",
            content: "Sí, empleamos fragancias hipoalergénicas especialmente formuladas para bebés, suaves y seguras.",
          },
          {
            title: "¿Las toallitas de Arrurrú tienen proteína de leche?",
            content: "No, nuestras toallitas no contienen proteína de leche, siendo adecuadas para pieles sensibles o alérgicas.",
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
    position: relative;
    padding-bottom: 10px;
  }
  
  .faq-title {
    text-align: center;
    font-size: 36px;
    font-family: "Arial", sans-serif;
    color: #E4016A;
    margin-bottom: 20px;
    font-weight: lighter;
  }
  
  .faq-title .highlight {
    color: #E4016A; /* Color para "Frecuentes" */
    font-weight: bold; /* Negrita para "Frecuentes" */
  }

  .faq-content {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
    width: 100%;
  }
  
  .faq-image {
  display: flex; 
  justify-content: center; 
  align-items: center; 
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
    border: 1px solid #f0f8ff;
    border-left-color: #AFD8EC;
    border-left-width: 10px;
    border-radius: 8px;
    margin-bottom: 10px;
    overflow: hidden;
  }
  
  .accordion-header {
    background: #f0f8ff;
    color: #333;
    padding: 15px;
    text-align: left;
    font-size: 18px;
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
    font-size: 16px;
    font-family: "Arial", sans-serif;

    line-height: 1.6;
    color: #444;
  }
  
  .accordion-icon {
    color: #E9006D;
    font-size: 20px;
    font-weight: bold;
    transition: transform 0.3s;
  }
  
  .accordion-icon.rotate {
    transform: rotate(45deg);
  }

  .bottom-line {
    width: 50%; 
    height: 4px; 
    background-color: #AFD8EC; 
    border-radius: 2px;
    position: absolute;
    bottom: -14px; 
    left: 50%;
    transform: translateX(-50%);
  }

  /* Responsive Design */
  @media (max-width: 768px) {
    .faq-content {
        grid-template-columns: 1fr;
    }

    .accordion-header {
        font-size: 15px;
    }

    .accordion-body {
        font-size: 14px;
    }
  }
  </style>
  