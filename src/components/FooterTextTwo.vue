<template>
  <div class="footer-text">
    <p><sup>*</sup>Azcona L. Cuidado de la piel del bebé. Atención especial. Farm Prof. 2005 Vol 19 (11); 54 - 57</p>
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
