<template>
    <footer class="footer">
      <h2 class="footer-title">Encuéntralos en:</h2>
      <div class="footer-grid">
        <div class="footer-container" @click="redirectTo('https://www.farmatodo.com.co/destacados/58413?utm_source=kraken&utm_medium=banner_home&utm_campaign=saleoff&utm_content=todas&utm_term=general30')">
          <img src="../assets/logos-sellos/logoFarmatodo.png" alt="Logo 1" class="footer-logo" />
        </div>
        <div class="footer-container" @click="redirectTo('https://www.exito.com/s?q=arrurru&sort=score_desc&page=0')">
          <img src="../assets/logos-sellos/logoExito.png" alt="Logo 2" class="footer-logo" />
        </div>
      </div>
    </footer>
  </template>
  
  <script>
  export default {
    name: "Footer",
    methods: {
    redirectTo(url) {
      window.location.href = url; // Redirección a la URL específica
    }
  }
  };
  </script>
  
  <style scoped>
  .footer {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 20px;
    /* background-color: #f8f8f8;  */
  }
  
  .footer-title {
    font-size: 1.8rem;
    font-weight: bold;
    text-align: center;
    margin-bottom: 30px;
    color: #244E75; 
    /* font-family: "Arial", sans-serif; */
  }
  
  .footer-grid {
    display: grid;
    grid-template-columns: 1fr; 
    gap: 20px;
    width: 100%;
    max-width: 1000px; 
  }
  
  @media (min-width: 768px) {
    .footer-grid {
      grid-template-columns: repeat(2, 1fr); 
    }
  }
  
  .footer-container {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px; 
    /* background-color: #ffffff;  */
    /* border: 1px solid #ddd; */ 
    border-radius: 10px; 
    cursor: pointer;
  }
  
  .footer-logo {
    max-width: 80%;
    max-height: 150px; 
    object-fit: contain;
  }
  </style>
  