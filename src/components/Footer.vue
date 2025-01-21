<template>
    <footer class="footer">
      <h2 class="footer-title">Encuéntralos en:</h2>
      <div class="footer-grid">
        <div class="footer-container">
          <img src="../assets/logos-sellos/logoFarmatodo.png" alt="Logo 1" class="footer-logo" />
        </div>
        <div class="footer-container">
          <img src="../assets/logos-sellos/logoExito.png" alt="Logo 2" class="footer-logo" />
        </div>
      </div>
    </footer>
  </template>
  
  <script>
  export default {
    name: "Footer",
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
    font-family: "Arial", sans-serif;
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
    background-color: #ffffff; 
    /* border: 1px solid #ddd; */ 
    border-radius: 10px; 
  }
  
  .footer-logo {
    max-width: 80%;
    max-height: 150px; 
    object-fit: contain;
  }
  </style>
  