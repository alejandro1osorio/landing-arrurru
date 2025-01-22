<template>
  <div class="benefits-container">
    <div class="header">
      <h1>Con Hidrosense, <span>hidrata y protege</span></h1>
    </div>
    <div class="description">
      <p>
        Los productos para el bebé deben proveer cuidado y ser seguros, debido a las condiciones
        de radiación solar, excesiva salivación, la orina y heces que son irritantes para la piel.
        Así que, deben contar con ingredientes que generen una película sobre la piel para mantenerla
        en buen estado.
      </p>
    </div>
    <div class="content">
      <div class="image-container">
        <img src="../assets/otros/ventaja.png" alt="Jojoba y biolípido" />
      </div>
      <div class="composition-wrapper">
        <div class="composition">
          <div class="composition-biomimetica">
            <h2>Composición Biomimética:</h2>
            <ul>
              <li>Propiedades para el balance en la microbiota.</li>
              <li>Compromiso con la sostenibilidad.</li>
            </ul>
          </div>
          <div class="characteristics">
            <h2>Principales características:</h2>
            <ul>
              <li>Componente que se encuentra <strong>naturalmente en la piel humana</strong>.</li>
              <li><strong>100% de origen natural.</strong> Certificado Ecocert.</li>
              <li>Máxima suavidad para el bebé.</li>
              <li>Hidratante natural.</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
    <div class="benefits">
      <h2 style="text-align: center;">Beneficios</h2>
      <div class="cards">
        <div class="card">Suave hidratación con biolípidos naturales.</div>
        <div class="card">Protege y restaura la humedad natural de la piel.</div>
        <div class="card">Ayuda a restaurar la película hidrolipídica que protege al bebé.</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Benefits",
};
</script>

<style scoped>
.benefits-container {
  display: grid;
  grid-template-rows: auto auto 1fr auto;
  gap: 1rem;
  padding: 2rem;
}

.header {
  text-align: center;
}

.header h1 {
  font-size: 2rem;
  font-weight: bold;
}

.header span {
  color: #ff4081;
}

.description {
  text-align: center;
  font-size: 1rem;
}

.content {
  display: flex;
  gap: 1rem;
}

.image-container {
  flex: 3;
  display: flex;
  justify-content: center;
  align-items: center;
}

.image-container img {
  max-width: 100%;
  height: auto;
}

.composition-wrapper {
  flex: 2;
  display: flex;
  justify-content: center;
  align-items: center;
}

.composition {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  text-align: left;
}

.composition h2 {
  font-size: 1.2rem;
  color: #ff4081;
}

.composition ul {
  list-style-type: disc;
  margin: 0;
  padding-left: 1.5rem;
}

.benefits {
  text-align: left;
  width: 60%;
}

.benefits h2 {
  font-size: 1.5rem;
  margin-bottom: 1rem;
}

.cards {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1rem;
}

.card {
  background-color: #f8f8f8;
  padding: 1rem;
  border-radius: 8px;
  text-align: center;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

@media (max-width: 768px) {
  .content {
    flex-direction: column;
  }

  .cards {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 480px) {
  .content {
    flex-direction: column;
  }

  .cards {
    grid-template-columns: 1fr;
  }
}
</style>
