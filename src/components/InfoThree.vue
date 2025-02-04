<template>
  <div class="container">
    <h1 class="title">Momento del <strong style="border-bottom: 5px solid #e91e63">Cuidado de la Colita</strong></h1>
    <p class="description">El área del pañal suele irritarse con facilidad, por lo que es clave el uso de toallitas que
      incorporen detergentes suaves para <strong style="color: #e91e63;">mantener intacto el manto hidrolipídico</strong> y cremas
protectoras, que como su nombre lo indica, forman una película protectora frente a las
agresiones de factores externos<sup>*</sup>.</p>
    <img src="../assets/otros/baby2.png" alt="Descripción de la imagen" class="corner-image">
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
  name: "InfoThree",
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
  font-size: 2.6rem;
  font-weight: 500;
  margin-bottom: 10px;
  color: #234e76;
}

.description {
  font-size: 1.2rem;
  color: #234e76;
  text-align: center;
  padding: 0 100px; /* Agregué padding a los lados */
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
    top: 190px;
    right: 220px;
  }

  .bottom-right-images {
    bottom: 10px;
    right: 290px;
  }

  .extra-top-image {
    width: 540px;
  }
}

/* Media query para computadoras portátiles */
@media (max-width: 1440px) {
  .corner-image {
    height: 600px;
  }
  .top-right-image {
    top: 244px;
    right: 70px;
  }
  .bottom-right-images{
    bottom: 10px;
    right: 90px;
  }
  .extra-image {
    width: 190px;
  }
  .extra-top-image {
    width: 440px;
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
    padding: 0 42px;
    text-align: justify;
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
  .container {
    height: 164vh;
  }
  .description {
    padding: 0 42px;
    text-align: justify;
  }
  .top-right-image {
    width: 310px;
    left: 44px;
    top: 22%;
  }
  .extra-top-image {
    width: 400px;
  } /* cambio aquí */
  .bottom-right-images {
    bottom: 80px;
    left: 80px;
  }
  .top-right-image, .bottom-right-images {
    display: grid;
    grid-template-rows: auto auto;
    justify-content: center;
    align-items: center;
    margin-top: 390px;

    text-align: center;
  }
  .extra-top-image, .extra-image {
    width: 270px;
    margin: 0 auto -110px auto;
  }
  .corner-image {
    height: 250px;
  }
}

/* Media query para pantallas pequeñas móviles en horizontal */
@media (min-width: 900px) and (max-width: 940px) and (orientation: landscape) {
  .top-right-image {
    visibility: hidden;
  }
  .bottom-right-images {
    visibility: hidden;
  }
} 

/* Media query para tablets pequeñas */
@media (min-width: 1000px) and (max-width: 1100px) {
  .top-right-image {
    right: 0;
  }
  .extra-top-image {
    width: 430px;
  }
  .bottom-right-images {
    right: 80px;
    bottom: 0;
  }
  .extra-image {
    width: 140px;
  }
}
</style>
