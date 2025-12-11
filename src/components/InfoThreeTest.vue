<template>
  <div class="parent" id="50color">
    <div class="div1">
      <div class="title-wrapper">
        <h1 class="title">
          Momento del <br><strong>Cuidado de la <strong style="border-bottom: 5px solid #e91e63;">Colita</strong></strong>
        </h1>

        <p class="subtitle">
          El área del pañal se irrita fácilmente, por eso se aconsejan toallitas suaves que no dañen el manto hidrolipídico. Las cremas protectoras ayudan creando una barrera frente a agresiones externas.
        </p>
      </div>
    </div>

    <div class="div2">
      <img src="../assets/otros/baby3.png" alt="Placeholder Image" class="image" />
    </div>

    <div class="div3">
      <img src="../assets/otros/info-toallas.png" alt="Placeholder Image" class="image-centered" />
    </div>

    <div class="div4">
      <img src="../assets/logos-sellos/grupo-sellos.png" alt="Placeholder Image" class="image-centered" />
    </div>
  </div>
</template>

<script>
export default {
  name: "GridLayout"
};
</script>

<style scoped>
.parent {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  grid-template-rows: repeat(5, 1fr);
  grid-column-gap: 0px;
  grid-row-gap: 0px;
  width: 100%;
  height: 100vh;
  padding: 0;
  box-sizing: border-box;
}

.div1 {
  grid-area: 1 / 1 / 2 / 13;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  text-align: center;
  margin: 0;
  position: relative;
}

.title-wrapper {
  max-width: 700px;
  padding: 0 16px;
}

.div1 .title {
  font-size: 2em;
  font-weight: 300;
  color: #214F79;
  margin-bottom: 0.4em;
}

.subtitle {
  font-size: 1rem;
  line-height: 1.4;
  color: #4b678a;
  margin: 0 auto;
}

.div2 {
  grid-area: 2 / 1 / 6 / 8;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
  margin: 0;
}

.div2 .image {
  width: 100%;
  height: 100%;
  object-fit: contain;
}

.div3 {
  grid-area: 2 / 9 / 5 / 12;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
  margin: 0;
}

.div3 .image-centered {
  max-width: 100%;
  max-height: 100%;
  object-fit: contain;
}

.div4 {
  grid-area: 5 / 8 / 6 / 13;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 80px;
  margin: 0;
}

.div4 .image-centered {
  max-width: 140%;
  max-height: 140%;
  object-fit: contain;
}

/* Monitores grandes */
@media screen and (min-width: 1400px) {
  .div1 .title {
    font-size: 2.4em;
  }
  .subtitle {
    font-size: 1.05rem;
  }
  .div4 {
    height: 110px;
  }
}

/* Portátiles medianos */
@media screen and (min-width: 1024px) and (max-width: 1399px) {
  .div1 .title {
    font-size: 2.1em;
  }
  .div4 {
    height: 90px;
  }
}

/* Móvil */
@media screen and (max-width: 768px) {
  .parent {
    grid-template-columns: repeat(6, 1fr);
    grid-template-rows: auto;
    height: 140vh;
  }

  .div1 {
    grid-area: 1 / 1 / 2 / 7;
  }

  .div1 .title {
    font-size: 1.5em;
  }

  .subtitle {
    font-size: 0.95rem;
  }

  .div2 {
    grid-area: 2 / 1 / 3 / 7;
  }

  .div3 {
    grid-area: 3 / 1 / 4 / 7;
  }

  .div4 {
    grid-area: 4 / 1 / 5 / 7;
  }
}
</style>
