<template>
  <div class="page-content">
    <h1>Página 1</h1>
    <p>Contenido de la segunda página del slider.</p>
  </div>
</template>

<script>
export default {
  name: 'PageTwo',
};
</script>

<style scoped>
.page-content {
  width: 90%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  background-color: #10410b; /* Color claro de fondo */
  border-radius: 10px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}
</style>
