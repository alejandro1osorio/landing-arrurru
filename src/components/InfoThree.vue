<template>
  <div class="parent">
    <div class="div1"><h1>Momento del <br><strong>Cuidado de la <strong style="border-bottom: 5px solid #e91e63;">Colita</strong></strong></h1></div>
    <div class="div2">
      <p style="font-size: 20px;">
        El área del pañal suele irritarse con facilidad, por lo que es clave el uso de toallitas que incorporen detergentes suaves para <strong style="color: #e91e63;">mantener intacto el manto hidrolipídico</strong> y cremas protectoras, que como su nombre lo indica, forman una película protectora frente a las agresiones de factores externos<sup>*</sup>.
      </p>
    </div>
    <div class="div3"></div>
    <div class="div4">
      <img src="../assets/otros/info-crema.png" alt="Imagen 4" class="large-image" />
    </div>
    <div class="div5">
      <img src="../assets/logos-sellos/Arrurru (22).png" alt="Imagen 5" class="image" />
    </div>
    <div class="div6">
      <img src="../assets/logos-sellos/Arrurru (23).png" alt="Imagen 6" class="image" />
    </div>
  </div>
</template>

<style scoped>
.parent {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  grid-template-rows: repeat(8, 1fr);
  gap: 5px;
  width: 100%;
  height: 110vh;
  padding: 10px;
  background-color: #f3f3f3;
}

h1 {
  font-weight: 500;
  color: #214F79;
}

.div1 {
  grid-column: 4 / span 6;
  /* background-color: #ffcccb; */
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.4em;
  text-align: center;
}

.div2 {
  grid-column: 3 / span 8;
  grid-row-start: 2;
  /* background-color: #add8e6; */
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: justify;
  text-align-last: center;
  color: #214F79;
}

.div3 {
  grid-column: span 8;
  grid-row: 3 / span 8;
  /* background-color: #90ee90; */
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 16px;
  background-image: url('../assets/otros/baby3.png');
  background-size: contain;
  background-position: center;
  background-repeat: no-repeat;
}

.div4 {
  /* grid-column: 10 / span 3; */
  grid-column: 9 / span 3;
  grid-row: 3 / span 4;
  /* background-color: #ffa07a; */
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 16px;
}

.div5, .div6, .div4 {
  display: flex;
  align-items: center;
  justify-content: center;
}

.image {
  max-width: 95%;
  max-height: 95%;
  object-fit: contain;
}

.large-image {
  max-width: 140%;
  max-height: 140%;
  object-fit: contain;
}

.div5 {
  grid-column: 9 / span 2;
  grid-row: 7 / span 2;
  /* background-color: #9370db; */
}

.div6 {
  grid-column: 11 / span 2;
  grid-row: 7 / span 2;
  /* background-color: #f4a460; */
}

@media (max-width: 768px) {
  .parent {
    display: grid;
    grid-template-columns: repeat(6, 1fr);
    grid-template-rows: auto;
    gap: 5px;
    height: auto;
  }
  h1 {
    font-size: 1.5em;
  }
  p {
    padding: 0 27px;
  }
  .div3 {
    visibility: hidden;
  }
  .div1, .div2, .div3 {
    grid-column: span 6;
    width: 100%;
  }
  .div4, .div5, .div6 {
    grid-column: span 5;
    grid-row: auto;
    width: 100%;
    margin-left: 36px;
  }
  .large-image {
    max-width: 120%;
    max-height: 120%;
  }
  .image {
    max-width: 90%;
    max-height: 90%;
  }
}
</style>
