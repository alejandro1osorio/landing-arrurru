<template>
  <div class="container">
    <h1 class="title">Momento del Masaje</h1>
    <p class="description">Para la piel y pelo del bebé es de gran importancia usar productos limpiadores suaves,
      para mantener las propiedades y características saludables.</p>
    <img src="../assets/otros/baby1.png" alt="Descripción de la imagen" class="corner-image">
    <div class="top-right-image">
      <img src="../assets/otros/info-shampoo.png" alt="Imagen superior derecha" class="extra-top-image">
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
  width: 470px;
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
  width: 220px;
  height: auto;
  object-fit: contain;
}

/* Media query para pantallas y monitores muy grandes */
@media (min-width: 1920px) {
  .top-right-image {
    top: 125px;
    right: 250px;
  }

  .bottom-right-images {
    bottom: 10px;
    right: 290px;
  }

  .extra-top-image {
    width: 520px;
  }
}

/* Media query para computadoras portátiles */
@media (max-width: 1440px) {
  .corner-image {
    height: 600px;
  }
  .top-right-image {
    top: 195px;
    right: 90px;
  }
  .bottom-right-images{
    bottom: 10px;
    right: 90px;
  }
  .extra-image {
    width: 190px;
  }
  .extra-top-image {
    width: 400px;
  }
}

/* Media query para tablets medianas */
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

/* Media query para móviles grandes */
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

/* Media query para móviles pequeños */
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
