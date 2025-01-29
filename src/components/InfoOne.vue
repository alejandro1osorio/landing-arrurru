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
  justify-content: space-between;
  align-items: center;
  width: 100%;
  height: 100vh; /* Manteniendo la altura del contenedor principal */
  text-align: center;
  box-sizing: border-box;
  background-color: #d8b0b0b0;
  position: relative;
  padding-top: 20px;
}

.text-container {
  width: 100%;
  text-align: center;
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
  position: absolute;
  bottom: 0;
  left: 0;
  width: 90%;
  height: 450px; /* Aumentado aún más el tamaño del contenedor */
  background-color: rgba(255, 255, 255, 0.8);
  border-top-right-radius: 20px;
  box-shadow: 0 -2px 10px rgba(0, 0, 0, 0.1);
}

@media (max-width: 768px) {
  .bottom-container {
    height: 350px; /* Ajuste responsivo para pantallas más pequeñas */
    width: 95%;
  }
}

@media (max-width: 480px) {
  .bottom-container {
    height: 300px; /* Ajuste responsivo para móviles */
    width: 100%;
  }
}

@media (min-width: 1440px) {
  .bottom-container {
    height: 600px; /* Ajuste para monitores grandes */
    width: 85%;
  }
}

@media (min-width: 1920px) {
  .bottom-container {
    height: 780px; /* Ajuste para monitores muy grandes */
    width: 95%;
  }
}
</style>
