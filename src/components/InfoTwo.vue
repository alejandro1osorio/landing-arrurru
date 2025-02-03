<template>
  <div class="container">
    <h1 class="title">Momento del Masaje</h1>
    <p class="description">La piel de los recién nacidos experimenta cambios significativos en su entorno tras el nacimiento, y su hidratación puede disminuir rápidamente apenas se da el alumbramiento1. Usar regularmente emolientes ayuda a proteger y mantener la salud de la piel del bebé, reduciendo el riesgo de dermatitis atópica o seborreica, especialmente en bebés con antecedentes familiares de enfermedades cutáneas1.</p>
    <img src="../assets/otros/baby2.png" alt="Descripción de la imagen" class="corner-image">
    <div class="top-right-image">
      <img src="../assets/otros/info-crema.png" alt="Imagen superior derecha" class="extra-top-image">
    </div>
    <div class="bottom-right-images">
      <img src="../assets/logos-sellos/Arrurru (22).png" alt="Imagen extra 1" class="extra-image">
      <img src="../assets/logos-sellos/Arrurru (23).png" alt="Imagen extra 2" class="extra-image">
    </div>
  </div>
</template>

<script>
export default {
  name: "InfoTwo",
};
</script>

<style scoped>
.container {
  background: #5e434359;
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

.top-right-image {
  position: absolute;
  top: 10px;
  right: 10px;
}

.extra-top-image {
  width: 120px;
  height: auto;
  object-fit: contain;
}

.bottom-right-images {
  position: absolute;
  bottom: 10px;
  right: 10px;
  display: flex;
  gap: 10px;
}

.extra-image {
  width: 100px;
  height: auto;
  object-fit: contain;
}

@media (max-width: 1440px) {
  .corner-image {
    height: 600px;
  }
  .extra-image {
    width: 80px;
  }
  .extra-top-image {
    width: 100px;
  }
}

@media (max-width: 1024px) {
  .corner-image {
    height: 500px;
  }
  .extra-image {
    width: 70px;
  }
  .extra-top-image {
    width: 90px;
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
  .extra-image {
    width: 60px;
  }
  .extra-top-image {
    width: 80px;
  }
}

@media (max-width: 480px) {
  .corner-image {
    height: 250px;
  }
  .extra-image {
    width: 50px;
  }
  .extra-top-image {
    width: 70px;
  }
}
</style>
