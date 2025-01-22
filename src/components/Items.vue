<template>
  <div class="grid-container">
    <div class="grid-item item1">
      <h2>El cuidado de la piel de los recién nacidos favorece el buen funcionamiento y su maduración después del nacimiento<sup>1</sup></h2>
    </div>
    <div class="grid-item item2">
      <p>
        Recientes investigaciones señalan que el uso diario de emolientes cutáneos desde el nacimiento del bebé a término es un factor protector en la prevención de la dermatitis atópica<sup>1</sup>.
      </p>
    </div>
    <div class="grid-item item3">
      <img src="../assets/otros/item1.png" alt="Imagen 3" />
    </div>
    <div class="grid-item item4">
      <img src="../assets/otros/item2.png" alt="Imagen 4" />
    </div>
    <div class="grid-item item5">
      <img src="../assets/otros/item3.png" alt="Imagen 5" />
    </div>
    <div class="grid-item item6">
      <p>
        En el cuidado del recién nacido, es fundamental prestar atención especial a los siguientes aspectos: el baño, la hidratación de la piel, el cuidado del cordón umbilical y la zona del pañal.
      </p>
    </div>
    <div class="grid-item item7-9">
      <div class="image-container">
        <img src="../assets/logos-sellos/logo-arrurru.png" alt="Imagen 7" />
      </div>
      <div class="text-container">
        <p>
          <strong>Arrurú</strong> es una marca experta en el cuidado del bebé en las diferentes etapas que cuenta con una línea completa de productos suaves, seguros, hipoalergénicos, con el pH ideal para la piel del bebé que no irrita los ojos<sup>*</sup>, dermatológicamente comprobados, certificados y recomendados por dermatólogos y pediatras.
        </p>
        <small>
          <sup>1</sup>Que hay de nuevo en el cuidado de la piel del recién nacido a término, Johnson E. Hunt R. Infant skin care: updates and recommendations. Curr Opin Pediatr. 2019, 31:476-481.
        </small>
      </div>
    </div>
  </div><!-- test -->
</template>

<script>
export default {
  name: "Items",
};
</script>

<style scoped>
.grid-container {
  display: grid;
  gap: 16px;
  grid-template-columns: repeat(3, 1fr);
  padding: 24px; /* Aumentado el margen interior */
}

.grid-item {
  padding: 16px;
  border: 1px solid #ddd;
  border-radius: 8px;
  background-color: #f9f9f9;
}

.item1,
.item2 {
  grid-column: span 3;
  text-align: center;
}

.item6 {
  grid-column: span 3;
  text-align: center;
}

.item7-9 {
  grid-column: span 3;
  display: flex;
  align-items: flex-start;
  gap: 16px;
}

.image-container img {
  width: 150px;
  height: auto;
  border-radius: 8px;
}

.text-container {
  flex: 1;
}

img {
  width: 100%;
  height: auto;
  border-radius: 8px;
}

/* Responsive styles */
@media (max-width: 768px) {
  .grid-container {
    grid-template-columns: 1fr;
  }

  .grid-item.item3,
  .grid-item.item4,
  .grid-item.item5 {
    grid-column: span 2; /* Cada imagen ocupa toda la fila en móviles */
  }

  .item7-9 {
    flex-direction: column;
    align-items: center;
    text-align: center;
  }

  .image-container img {
    width: 100px; /* Tamaño reducido para móviles */
  }
}
</style>
