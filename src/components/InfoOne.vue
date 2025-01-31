<template>
  <div class="info-container">
    <div class="text-container">
      <h1 class="title">Momento del Baño</h1>
      <p class="description">
        Para la piel y pelo del bebé es de gran importancia usar productos limpiadores suaves,
        para mantener las propiedades y características saludables.
      </p>
    </div>
    <div class="bottom-container">
      <p>Contenido adicional aquí</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "InfoOne"
};
</script>

<style scoped>
.info-container {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start; /* Asegura que todo toque el borde izquierdo */
  width: 100%;
  min-height: 100vh;
  text-align: center;
  box-sizing: border-box;
  background-color: #d8b0b0b0;
  position: relative;
}

.text-container {
  width: 100%;
  text-align: center;
  margin-bottom: 20px; /* Espacio adicional para evitar superposición */
}

.title {
  font-size: 2rem;
  font-weight: bold;
  margin-bottom: 10px;
}

.description {
  font-size: 1.2rem;
  color: #666;
}

.bottom-container {
  display: grid;
  place-items: center;
  width: 90%;
  min-height: 600px;
  background-color: rgba(255, 255, 255, 0.8);
  border-top-right-radius: 20px;
  box-shadow: 0 -2px 10px rgba(0, 0, 0, 0.1);
  margin-top: 5px; /* Asegura que esté al final sin sobreponer */
  align-self: flex-start; /* Asegura que toque el borde izquierdo */
}

@media (min-width: 600px) and (max-width: 1024px) {
  .bottom-container {
    min-height: 600px; /* Aumento de altura solo en tablets medianas */
    width: 92%;
  }
}

@media (max-width: 768px) {
  .bottom-container {
    min-height: 400px;
    width: 95%;
  }
}

@media (max-width: 480px) {
  .bottom-container {
    min-height: 320px;
    width: 100%;
  }
}

@media (min-width: 1025px) {
  .bottom-container {
    min-height: 630px; /* Mantiene la altura original en computadoras */
  }
}

@media (min-width: 1440px) {
  .bottom-container {
    min-height: 720px;
    width: 85%;
  }
}

@media (min-width: 1920px) {
  .bottom-container {
    min-height: 800px;
    width: 95%;
  }
}
</style>
