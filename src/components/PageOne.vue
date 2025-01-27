<template>
  <div class="page-grid">
    <h1 class="page-title">Shampoo y Baño Líquido Recién Nacido</h1>
    <div class="image-structure">
      <!-- Contenedor superior izquierdo -->
      <div class="box top-left">Contenido Superior Izquierdo</div>
      <!-- Contenedor inferior izquierdo -->
      <div class="box bottom-left">Contenido Inferior Izquierdo</div>
      <!-- Imagen en el centro -->
      <div class="image-container">
        <img src="../assets/productos/shampoo2-1.png" alt="Shampoo y Baño Líquido Recién Nacido" />
      </div>
      <!-- Contenedor superior derecho -->
      <div class="box top-right">Contenido Superior Derecho</div>
      <!-- Contenedor inferior derecho -->
      <div class="box bottom-right">Contenido Inferior Derecho</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PageOne',
};
</script>

<style scoped>
.page-grid {
  display: grid;
  grid-template-rows: auto 1fr;
  justify-items: center;
  align-items: center;
  width: 100%;
  height: 100%;
  padding: 20px;
  box-sizing: border-box;
  gap: 20px;
  background-color: #f0f8ff;
}

.page-title {
  font-size: 1.8rem;
  font-weight: bold;
  text-align: center;
  color: #333;
}

.image-structure {
  display: grid;
  grid-template-areas:
    "top-left image top-right"
    "bottom-left image bottom-right";
  grid-template-columns: auto 1fr auto;
  grid-template-rows: auto auto;
  gap: 20px;
  align-items: center;
  justify-items: center;
  width: 100%;
}

.image-container {
  grid-area: image;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  max-width: 300px;
}

.image-container img {
  max-width: 100%;
  height: auto;
  border-radius: 10px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.box {
  width: 150px;
  height: 80px;
  background-color: #e0e0e0;
  border-radius: 10px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.top-left {
  grid-area: top-left;
}

.bottom-left {
  grid-area: bottom-left;
}

.top-right {
  grid-area: top-right;
}

.bottom-right {
  grid-area: bottom-right;
}
</style>
