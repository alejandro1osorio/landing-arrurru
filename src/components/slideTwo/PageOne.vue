<template>
  <div class="page-grid">
    <!-- <InfoOne /> -->
    <h1 class="page-title"><strong>Crema</strong> Recién Nacido</h1>
    <div class="image-structure">
      <!-- Contenedor superior izquierdo -->
      <!-- Imagen en el centro -->
      <div class="image-container">
        <div class="container-item">
          <div class="box top-left" style="flex-direction: row;">
            <p>Con <strong>Hidrosense</strong> (Mezcla única de Jojoba + Biolípido de origen natural en nuestro portafolio)</p>
            <img src="../../assets/beneficios-productos/hidrosense.png" alt="Hidrosense" style="z-index: 2; transform: translate(0%, 0%) scale(1.07);"/>
            <span class="line right"></span>
          </div>
          <!-- Contenedor inferior izquierdo -->
          <div class="box bottom-left" style="flex-direction: row;">
            <p>Con extracto de algodón que cuida la piel.</p>
            <img src="../../assets/beneficios-productos/algodon.png" alt="Algodón" style="z-index: 2; transform: translate(0%, 0%) scale(1.07);" />
            <span class="line right"></span>
          </div>
        </div>
        
        <img src="../../assets/productos/crema.png" alt="Shampoo y Baño Líquido Recién Nacido" style="padding: 0 26px;"/>
        
        <div>
          <div class="box top-right">
            <img src="../../assets/beneficios-productos/quimicos.png" alt="Sin Parabenos" style="z-index: 2; transform: translate(0%, 2%) scale(1.07);" />
            <p style="font-size: 0.7rem;"><strong>Libre de</strong> Parabenos y Colorantes.</p>
            <span class="line left"></span>
          </div>
          <!-- Contenedor inferior derecho -->
          <div class="box bottom-right">
            <img src="../../assets/beneficios-productos/irritacion.png" alt="No irrita ojos" style="z-index: 2; transform: translate(0%, 2%) scale(1.07);" />
            <p><strong>Con estudio de irritación dérmica.</strong> Aprobado y recomendado por pediatras y dermatólogos.</p>
            <span class="line left"></span>
          </div>
        </div>
      </div>
      <!-- Contenedor superior derecho -->
      
    </div>

    <div class="button-group">
      <button @click="setActiveTab('benefits')">Beneficios</button>
      <button @click="setActiveTab('usage')">Modo de uso</button>
      <button @click="setActiveTab('composition')">Composición</button>
    </div>
    <div v-if="activeTab" class="content-tab">
      <div class="tab-header">
        <button class="close-btn" @click="closeTab">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M6 18L18 6M6 6L18 18" stroke="#E4016A" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </button>
      </div>

      <p v-if="activeTab === 'benefits'" class="text-tab">
        La piel del recién nacido requiere de mayor cuidado, por eso Arrurrú Crema Recién Nacido esta
        formulado especialmente diseñada con Hidrosense (Mezcla única de Jojoba + Biolípido de
        origen natural en nuestro portafolio) y extracto algodón, que cuidan la delicada piel del bebé,
        nutriéndola y protegiéndola desde el primer día. <strong style="color: #E4016A;">Hidrata la piel del bebé hasta por 24 horas
          ayudando a retener su humectación natural.</strong><br>
        <strong style="color: #E4016A;">•</strong> Hipoalergénico y dermatológicamente testeado. <br>
        <strong style="color: #E4016A;">•</strong> Libre de parabenos y colorantes adicionados. <br>
        <strong style="color: #E4016A;">•</strong> Cuida especialmente la delicada piel de tu bebé.
      </p>
      <p v-if="activeTab === 'usage'">Aplica una pequeña cantidad de la crema en la mano y deslizar en todo el cuerpo de tu bebe con un suave y estimulante masaje después del baño.</p>
      <p v-if="activeTab === 'composition'">Aqua (Water), Glycerin, Cetearyl Alcohol, Dicaprylyl Carbonate, Glyceryl Stearate / Ceteareth - 20 / Ceteareth - 12 / Cetearyl Alcohol / Cetyl Palmitate, Octyl Dodecanol, Butyrospermum Parkii (Shea Butter), Benzyl Alcohol / Sodium Benzoate / Potassium Sorbate, Dimethicone, Pentaerythrityl Distearate, Parfum (Fragrance), Carbomer, Coco-Glucoside / Glyceryl Oleate, Simmondsia Chinensis (Jojoba) Seed Oil, Sodium Gluconate, Sodium Hydroxide, Mannitol / Ammonium Glycyrrhizate / Caffeine / Zinc Gluconate / Aesculus Hippocastanum (Horse Chestnut) Seed Extract, Xanthan Gum, Glycerin / Aqua (Water)  / Gossypium Herbaceum (Cotton) Seed Extract.</p>
    </div>

    <footer>
      <p class="text-footer">Con estudio en <strong>pieles sensibles</strong></p>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'PageOne',
  data() {
    return {
      activeTab: '',
    };
  },
  methods: {
    setActiveTab(tab) {
      this.activeTab = tab;
    },
    closeTab() {
      this.activeTab = '';
    }
  },
};
</script>

<style scoped>
/* .info-container {
  text-align: center;
  padding: 10px;
  border-radius: 10px;
  margin-bottom: 10px;
} */

.page-grid {
  display: grid;
  grid-template-rows: auto 1fr;
  justify-items: center;
  align-items: center;
  width: 100%;
  height: 100%;
  /* padding: 0 20px; */
  box-sizing: border-box;
  /* gap: 20px; */
  background-color: #F3F3F3;
}

.page-title {
  font-size: 1.8rem;
  font-weight: 300;
  text-align: center;
  color: #214F79;
}

.image-structure {
  display: grid;
  grid-template-areas:
    "top-left image top-right"
    "bottom-left image bottom-right";
  /* grid-template-columns: auto 1fr auto; */
  grid-template-columns: 1fr 0.4fr 1fr;
  grid-template-rows: auto auto;
  gap: 20px;
  align-items: center;
  justify-items: center;
  width: 100%;
}

.image-container {
  grid-area: image;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 130%;
  max-width: 300px;
}

.image-container img {
  max-width: 100%;
  height: auto;
  border-radius: 10px;
  /* box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); */
}

.box {
  display: flex;
  align-items: center;
  width: 280px; /* Aumentado el ancho de los contenedores */
  height: auto;
  background-color: #ffffff;
  border-radius: 10px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  gap: 8px; /* Ajustado el espaciado */
  /* padding: 8px; */
  position: relative; /* Necesario para las líneas */
}

.box img {
  max-width: 100px; /* Disminuido el tamaño de las imágenes */
  height: auto;
}

.box p {
  font-weight: 500;
  color: #214F79;
  font-size: 0.8rem; /* Reducido el tamaño del texto */
}

/* Líneas decorativas */
.line {
  position: absolute;
  width: 100px;
  height: 2px;
  background-color: #7BA0AD;
  top: 50%;
  transform: translateY(-50%);
}

.line.right {
  right: -94px;
}

.line.left {
  left: -94px;
}

.line::after {
  content: '';
  position: absolute;
  width: 20px;
  height: 20px;
  background-color: #7AA0AD;
  border: 2px solid #CFE1ED;
  border-radius: 50%;
  top: 50%;
  transform: translateY(-50%);
}

.line.right::after {
  right: -10px;
}

.line.left::after {
  left: -10px;
}

.top-left {
  grid-area: top-left;
  flex-direction: row-reverse; /* Imagen a la derecha */
  padding-left: 20px;
  border-radius: 57px 59px 59px 17px;
  margin-bottom: 50%;
}

.bottom-left {
  grid-area: bottom-left;
  flex-direction: row-reverse; /* Imagen a la derecha */
  padding-left: 20px;
  border-radius: 57px 59px 59px 17px;
}

.top-right {
  grid-area: top-right;
  flex-direction: row; /* Imagen a la izquierda */
  padding-right: 20px;
  border-radius: 100px 100px 35px 100px;
  margin-bottom: 50%;
}

.bottom-right {
  grid-area: bottom-right;
  flex-direction: row; /* Imagen a la izquierda */
  padding-right: 20px;
  border-radius: 100px 100px 35px 100px;
}

.content-tab {
  border: 2px solid #E31C79;
  border-radius: 0px 12px 12px 12px;
  width: 60%;
  padding: 20px;
  background: #F3F3F3;
}

.content-tab, p {
  font-weight: 400;
  color: #214F79;
}

.button-group {
  display: flex;
  gap: 10px;
}

button {
  padding: 5px 10px;
  font-size: 0.9rem;
  border: none;
  border-radius: 5px;
  background-color: #DEE5E7;
  color: #214F79;
  cursor: pointer;
  transition: background-color 0.3s;
}

button:hover {
  color: white;
  background-color: #7BA0AD;
}

button:active,
button:focus {
  background-color: #7BA0AD;
  color: #fff;
}

.tab-header {
  display: flex;
  justify-content: flex-end;
  padding: 5px;
}
.close-btn {
  background: transparent;
  border: none;
  font-size: 1.5rem;
  cursor: pointer;
  color: #E4016A;
}

footer {
  background: #48CDDE; /* #7AA0AD */
  font-size: 1.5rem;
  width: 100%; 
  margin-top: 30px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.text-footer {
  color: #fff;
}

@media (max-width: 768px) {
  /* .box {
    visibility: hidden;
  } */

  .image-structure {
    transform: scale(0.39);
    margin-top: -182px;
  }

  .button-group {
    margin-top: -278px;
  }

  .content-tab {
    margin-top: -126px;
  }

  .content-tab, p {
    font-size: 0.9rem;
  }
}
</style>