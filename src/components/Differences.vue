<template>
  <div class="differences-container">
    <!-- Contenedor izquierdo -->
    <div class="image-container">
      <img src="../assets/otros/differences.png" alt="Diferencias entre piel de bebé y adulto" />
    </div>

    <!-- Contenedor derecho -->
    <div class="text-container">
      <h1>Diferencias entre la piel de un recién nacido y un adulto.</h1>
      <p>
        La piel del recién nacido es <strong>verdaderamente extraordinaria</strong>,
        se caracteriza por su notable suavidad, tersura y uniformidad, ¿pero está
        preparada para sobrevivir en condiciones duras y hostiles después del
        nacimiento? Aunque la evidencia muestra la diferencia en la composición
        de la piel del recién nacido y la de un adulto, <strong>la piel de un bebé a término
        está lista para adaptarse fuera del vientre</strong> gracias a la barrera protectora que
        se desarrolla durante el último trimestre por el vérnix caseoso.
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
  max-width: 100%;
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
  font-size: 2rem; /* Ajuste del tamaño del título */
  margin-bottom: 1rem;
  color: #2c3e50;
  font-weight: 600;
  line-height: 1;
}

.text-container p {
  font-size: 1.2rem;
  text-align: justify;
  line-height: 1.8;
  margin-bottom: 1.5rem;
  font-weight: 400;
  line-height: 1;
}

.text-container small {
  font-size: 1rem;
  color: #7f8c8d;
  font-weight: 300;
  line-height: 1;
}

/* Responsividad */
@media screen and (max-width: 1180px) and (min-width: 800px) {
  .differences-container {
    grid-template-columns: 1fr; /* Cambia a una columna */
  }

  .image-container, .text-container {
    text-align: center;
  }
}

@media screen and (max-width: 768px) {
  .differences-container {
    grid-template-columns: 1fr;
  }

  .image-container, .text-container {
    text-align: center;
  }
}
</style>
