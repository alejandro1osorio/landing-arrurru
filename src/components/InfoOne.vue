<template>
  <div class="container">
    <h1 class="title">Título del Componente</h1>
    <p class="description">Este es un componente responsivo en Vue.js. Se adapta a diferentes tamaños de pantalla y ocupa el 100% del ancho disponible.</p>
    <img src="../assets/otros/baby1.png" alt="Descripción de la imagen" class="corner-image">
  </div>
</template>

<script>
export default {
  name: "ResponsiveComponent",
};
</script>

<style scoped>
.container {
  width: 100%;
  text-align: center;
  box-sizing: border-box;
  position: relative;
}

.title {
  font-size: 2rem;
  font-weight: bold;
  margin-bottom: 10px;
}

.description {
  font-size: 1.2rem;
  color: #555;
}

.corner-image {
  display: block;
  width: auto;
  height: 700px;
  object-fit: contain;
  margin-left: 0;
}

@media (max-width: 1440px) {
  .corner-image {
    height: 600px;
  }
}

@media (max-width: 1024px) {
  .corner-image {
    height: 500px;
  }
}

@media (max-width: 768px) {
  .title {
    font-size: 1.5rem;
  }
  .description {
    font-size: 1rem;
  }
  .corner-image {
    height: 400px;
  }
}

@media (max-width: 480px) {
  .corner-image {
    height: 250px;
  }
}
</style>
