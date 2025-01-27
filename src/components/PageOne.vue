<template>
  <div class="page-grid">
    <h1 class="page-title">Shampoo y Baño Líquido Recién Nacido</h1>
    <div class="image-container">
      <img src="../assets/productos/shampoo2-1.png" alt="Shampoo y Baño Líquido Recién Nacido" />
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
  max-width: 90%;
  word-wrap: break-word;
}

.image-container {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  max-width: 300px; /* Limita el tamaño máximo de la imagen */
  height: auto;
  overflow: hidden;
}

.image-container img {
  max-width: 100%;
  height: auto;
  border-radius: 10px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}
</style>
