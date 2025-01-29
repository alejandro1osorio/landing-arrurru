```vue
<!-- segunda version -->

<template>
  <div class="container">
    <h1 class="title">Título del Componente</h1>
    <div class="content">
      <!-- Contenedor Izquierdo -->
      <div class="side-box left-box">
        <p>Texto del contenedor izquierdo</p>
      </div>

      <!-- Contenedor Central -->
      <div class="center-box">
        <img src="../assets/productos/toallitas-humedas.png" alt="Imagen Central" />
      </div>

      <!-- Contenedor Derecho -->
      <div class="side-box right-box">
        <p>Texto del contenedor derecho</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ThreeColumnLayout",
};
</script>

<style scoped>
/* Estilos generales */
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  padding: 20px;
  width: 100%;
}

.title {
  font-size: 1.8rem;
  font-weight: bold;
  margin-bottom: 20px;
}

/* Contenedor principal */
.content {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  max-width: 1200px;
  gap: 20px;
}

/* Contenedor central */
.center-box {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #f3f3f3;
  border-radius: 10px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  overflow: hidden;
}

.center-box img {
  max-width: 70%; /* Reducido aún más el tamaño de la imagen */
  height: auto;
  object-fit: contain;
}

/* Contenedores laterales */
.side-box {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 250px;
  height: 250px;
  background-color: #ffffff;
  border-radius: 10px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  padding: 20px;
  text-align: center;
  font-size: 1rem;
}

/* Responsividad */
@media (max-width: 1024px) {
  .content {
    gap: 10px;
  }

  .center-box img {
    max-width: 85%;
  }
}

@media (max-width: 768px) {
  .content {
    flex-direction: column;
    gap: 15px;
  }

  .side-box,
  .center-box {
    width: 100%;
    max-width: 350px;
  }

  .center-box img {
    max-width: 65%;
  }
}

@media (max-width: 480px) {
  .center-box img {
    max-width: 55%;
  }
}
</style>


```