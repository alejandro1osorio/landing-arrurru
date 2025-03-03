<template>
  <div class="footer-text">
    <p>3.  Qué hay de nuevo en el cuidado de la piel del recién nacido a término Johnson E. Hunt R. Infant skin care: updates and <br> recommendations. Curr Opin Pediatr 2019, 31:476–481. &nbsp;&nbsp;4. Estudio para pieles sensibles en al línea recién nacido de Arrurrú
</p>
  </div>
</template>

<script>
export default {
  name: "FooterText",
};
</script>

<style scoped>
.footer-text {
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  font-size: 0.9em;
  line-height: 1;
  color: #666b70;
  padding: 0 20px;
  font-style: italic;
  /* background-color: rgba(255, 255, 255, 0.8); */
  width: 100%;
  max-width: 100%;
  overflow: hidden;
}

@media screen and (max-width: 768px) { 
  .footer-text {
    font-size: 0.8em;
    padding: 0px 0px;
  }
}
</style>
