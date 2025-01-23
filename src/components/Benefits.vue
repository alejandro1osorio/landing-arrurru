<template>
  <div class="benefits-container">
    <div class="header">
      <h1>Con Hidrosense, <span>hidrata y protege</span></h1>
    </div>
    <div class="description">
      <p>
        <span class="highlight">Los productos para el bebé deben proveer cuidado y ser seguros,</span> debido a las condiciones
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
      <h2 style="text-align: center;" class="benefits-title">Beneficios</h2>
      <div class="benefits-line"></div>
      <div class="cards">
        <div class="card"><strong>Suave hidratación</strong> con biolípidos naturales.</div>
        <div class="card"><strong>Protege y restaura</strong> la humedad natural de la piel.</div>
        <div class="card"><strong>Ayuda a restaurar</strong> la película hidrolipídica que protege al bebé.</div>
      </div>
    </div>
    <div class="footer">
      <p>*Azcona L. Cuidado de la piel del bebé. Atención especial. Farm Prof. 2005 Vol 19 (11); 54 - 57</p>
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
  grid-template-rows: auto auto 1fr auto auto;
  /* gap: 1rem; */ /* Comentado según la solicitud */
  padding: 0 3rem; /* Ajustar márgenes interiores laterales */
}

.header {
  text-align: center;
}

.header h1 {
  font-size: 3rem;
  font-weight: 300;
  color: #E31C79;
  line-height: 1.2;
}

.header h1 span {
  font-weight: bold;
}

@media (max-width: 768px) {
  .header h1 {
    font-size: 2.5rem;
  }
}

@media (max-width: 480px) {
  .header h1 {
    font-size: 2rem;
  }
}

.description {
  text-align: center;
  font-size: 1.4rem;
  color: #214F79;
  line-height: 1.6;
}

.description .highlight {
  color: #E31C79;
  font-weight: bold;
}

@media (max-width: 768px) {
  .description {
    font-size: 1.3rem;
  }
}

@media (max-width: 480px) {
  .description {
    font-size: 1.2rem;
  }
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
  font-size: 1.5rem;
  color: #E31C79;
}

.composition ul {
  list-style-type: disc;
  margin: 0;
  padding-left: 1.5rem;
  font-size: 1.2rem;
  color: #214F79;
}

@media (max-width: 768px) {
  .composition h2 {
    font-size: 1.4rem;
  }

  .composition ul {
    font-size: 1.1rem;
  }
}

@media (max-width: 480px) {
  .composition h2 {
    font-size: 1.3rem;
  }

  .composition ul {
    font-size: 1rem;
  }
}

.benefits {
  text-align: left;
  width: 60%;
}

.benefits-title {
  font-size: 1.5rem;
  margin-bottom: 1rem;
  color: #E31C79;
  text-align: center;
}

.benefits-line {
  width: 60%;
  height: 2px;
  background-color: #CFE1ED;
  margin: 0 auto 1rem auto;
}

.cards {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1rem;
  padding: 0 5rem;
}

.card {
  background-color: #EBEBEB;
  padding: 0.6rem;
  border-radius: 6px;
  text-align: center;
  font-size: 0.85rem;
  font-weight: 400;
  color: #214F79;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
}

.footer {
  text-align: center;
  font-size: 0.9rem;
  color: gray;
  margin-top: 1rem;
}

@media (max-width: 768px) {
  .content {
    flex-direction: column;
  }

  .cards {
    grid-template-columns: 1fr;
    padding: 0 3rem;
  }
}

@media (max-width: 480px) {
  .content {
    flex-direction: column;
  }

  .description {
    font-size: 0.9rem; /* Reducir tamaño del texto en pantallas móviles */
  }

  .benefits {
    display: contents; /* Ajuste para pantallas móviles */
  }

  .cards {
    grid-template-columns: 1fr;
    padding: 0 2rem;
  }
}
</style>
