<template>
  <div class="differences-container">
    <!-- Contenedor izquierdo -->
    <div class="image-container">
      <img src="../assets/otros/differences.png" alt="Diferencias entre piel de bebé y adulto" />
    </div>

    <!-- Contenedor derecho -->
    <div class="text-container">
      <h1>Diferencias entre la piel de <span style="color: #E31C79;">un recién nacido</span> y un adulto.</h1>
      <p>
        <strong style="color: #234D75;">La piel del recién nacido es</strong> <strong style="color: #E91980;">verdaderamente extraordinaria</strong>,
        se caracteriza por su notable suavidad, tersura y uniformidad, ¿pero está
        preparada para sobrevivir en condiciones duras y hostiles después del
        nacimiento? Aunque la evidencia muestra la diferencia en la composición
        de la piel del recién nacido y la de un adulto, <strong style="color: #234D75;">la piel de un bebé a término
        está lista para adaptarse fuera del vientre</strong> gracias a la barrera protectora que
        se desarrolla durante el último trimestre por el vérnix caseoso<sup>1</sup>.
      </p>
      <small>
        1.Visscher M. Hu P. Carr A. et al. Newborn infant skin gene expression:
        Remarkable differences versus adults. PLoS One. 2021 Oct 19;16(10)
      </small>
    </div>
  </div>
</template>

<script>
export default {
  name: "Differences",
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@100;200;300;400;500;600;700;800;900&display=swap');

.differences-container {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  align-items: center;
}

.image-container {
  display: flex;
  justify-content: center;
  align-items: center;
}

.image-container img {
  max-width: 110%; 
  height: auto;
  object-fit: cover;
}

.text-container {
  padding: 30px;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  font-family: 'Poppins', sans-serif; 
}

.text-container h1 {
  font-size: 2.5rem; 
  margin-bottom: 1rem;
  color: #214F79;
  font-weight: 600;
  line-height: 1;
}

.text-container p {
  font-size: 1.4rem; 
  color: #214F79;
  text-align: justify;
  margin-bottom: 1.5rem;
  font-weight: 400;
  line-height: 1.1;
}

.text-container small {
  font-size: 1.2rem; 
  color: #7f8c8d;
  font-weight: 300;
  line-height: 1.1;
}

/* Responsividad */
@media screen and (max-width: 1180px) and (min-width: 800px) {
  .differences-container {
    grid-template-columns: 1fr; /* Cambia a una columna */
  }

  .image-container, .text-container {
    text-align: center;
  }

  .image-container img {
    max-width: 100%; /* Ajusta el tamaño de la imagen en este rango */
  }

  .text-container h1 {
    font-size: 2.2rem; /* Ajusta el tamaño del título en este rango */
  }

  .text-container p {
    font-size: 1.3rem; /* Ajusta el tamaño del texto descriptivo */
  }

  .text-container small {
    font-size: 1.1rem; /* Ajusta el tamaño del texto pequeño */
  }
}

@media screen and (max-width: 768px) {
  .differences-container {
    grid-template-columns: 1fr;
  }

  .image-container, .text-container {
    text-align: center;
  }

  .image-container img {
    max-width: 100%; /* Ajusta el tamaño de la imagen para móviles */
  }

  .text-container h1 {
    font-size: 2rem; /* Ajusta el tamaño del título en móviles */
  }

  .text-container p {
    font-size: 1.2rem; /* Ajusta el tamaño del texto descriptivo */
  }

  .text-container small {
    font-size: 1rem; /* Ajusta el tamaño del texto pequeño */
  }
}
</style>
