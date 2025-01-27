<template>
  <div class="page-grid">
    <h1 class="page-title">Shampoo y Baño Líquido Recién Nacido</h1>
    <div class="image-structure">
      <!-- Contenedor superior izquierdo -->
      <div class="box top-left" style="flex-direction: row;">
        <p>Con Hidrosense (Mezcla única de Jojoba + Biolípido de origen natural en nuestro portafolio)</p>
        <img src="../assets/beneficios-productos/hidrosense.png" alt="Hidrosense" />
      </div>
      <!-- Contenedor inferior izquierdo -->
      <div class="box bottom-left" style="flex-direction: row;">
        <p>Con extracto de algodón que cuida la piel.</p>
        <img src="../assets/beneficios-productos/algodon.png" alt="Algodón" />
      </div>
      <!-- Imagen en el centro -->
      <div class="image-container">
        <img src="../assets/productos/shampoo2-1.png" alt="Shampoo y Baño Líquido Recién Nacido" />
      </div>
      <!-- Contenedor superior derecho -->
      <div class="box top-right">
        <img src="../assets/beneficios-productos/quimicos.png" alt="Sin Parabenos" />
        <p>Libre de parabenos, siliconas, sal (cloruro de sodio adicionado), colorantes (adicionados) y sulfatos.</p>
      </div>
      <!-- Contenedor inferior derecho -->
      <div class="box bottom-right">
        <img src="../assets/beneficios-productos/irritacion.png" alt="No irrita ojos" />
        <p>Delicado con los ojos
          del bebé, no los irrita.</p>
      </div>
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
  /* box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); */
}

.box {
  display: flex;
  align-items: center;
  width: 280px; /* Aumentado el ancho de los contenedores */
  height: auto;
  background-color: #ffffff;
  border-radius: 10px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  gap: 8px; /* Ajustado el espaciado */
  /* padding: 8px; */
}

.box img {
  max-width: 100px; /* Disminuido el tamaño de las imágenes */
  height: auto;
}

.box p {
  font-size: 0.8rem; /* Reducido el tamaño del texto */
}

.top-left {
  grid-area: top-left;
  flex-direction: row-reverse; /* Imagen a la derecha */
  padding-left: 20px;
  border-radius: 0 0 0 0;
}

.bottom-left {
  grid-area: bottom-left;
  flex-direction: row-reverse; /* Imagen a la derecha */
  padding-left: 20px;
  border-radius: 0 0 0 0;
}

.top-right {
  grid-area: top-right;
  flex-direction: row; /* Imagen a la izquierda */
  padding-right: 20px;
  border-radius: 0 0 0 0;
}

.bottom-right {
  grid-area: bottom-right;
  flex-direction: row; /* Imagen a la izquierda */
  padding-right: 20px;
  border-radius: 0 0 0 0;
}
</style>
