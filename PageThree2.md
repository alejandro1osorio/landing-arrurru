```vue

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
        <span class="line left"></span>
        <span class="line left second"></span>
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
  position: relative;
  padding: 20px;
}

.center-box img {
  max-width: 65%; /* Ajustado el tamaño para evitar ocultamiento */
  height: auto;
  object-fit: contain;
  z-index: 1;
}

/* Líneas decorativas */
.line {
  position: absolute;
  width: 70px;
  height: 2px;
  background-color: #7BA0AD;
  top: 40%;
  transform: translateY(-50%);
  z-index: 2;
}

.line.left {
  left: -35px;
}

.line.left.second {
  left: -75px;
  top: 60%;
}

/* Añadir el círculo al final de cada línea */
.line::after {
  content: '';
  position: absolute;
  width: 15px;
  height: 15px;
  background-color: #7AA0AD;
  border: 2px solid #CFE1ED;
  border-radius: 50%;
  top: 50%;
  transform: translateY(-50%);
}

.line.left::after {
  right: -10px;
}

.line.left.second::after {
  right: -10px;
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
    max-width: 75%;
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
    max-width: 60%;
  }

  .line {
    width: 50px;
  }

  .line.left {
    left: -25px;
  }

  .line.left.second {
    left: -55px;
  }
}

@media (max-width: 480px) {
  .center-box img {
    max-width: 50%;
  }

  .line {
    width: 40px;
  }

  .line.left {
    left: -20px;
  }

  .line.left.second {
    left: -45px;
  }
}
</style>


```