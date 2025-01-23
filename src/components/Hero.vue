<template>
  <section class="hero">
    <img src="../assets/logos-sellos/logo-arrurru.png" alt="Centered Image" class="centered-image" />
  </section>
</template>

<script>
export default {
  name: "Hero",
};
</script>

<style scoped>
.hero {
  height: 100vh; /* Full viewport height */
  background-image: url('../assets/otros/hero.png'); /* Replace with your image URL */
  background-size: cover; /* Ensures the image covers the entire section */
  background-position: center; /* Centers the image */
  background-repeat: no-repeat; /* Prevents tiling */
  display: flex;
  align-items: flex-end; /* Align content to the bottom */
  justify-content: center; /* Center horizontally */
  position: relative;
  overflow: hidden; /* Ensures no overflow */
}

.centered-image {
  position: relative;
  z-index: 2;
  width: 20%; /* Adjust width for responsiveness */
  max-width: 200px; /* Limit maximum size */
  height: auto; /* Maintain aspect ratio */
  margin-bottom: 2rem; /* Add space from the bottom */
}

@media (max-width: 768px) {
  .centered-image {
    width: 35%; /* Increase size for smaller screens */
    max-width: 175px;
    margin-bottom: 3rem; /* Increase margin for smaller screens */
  }
}

@media (max-width: 480px) {
  .centered-image {
    width: 50%; /* Further increase size for very small screens */
    max-width: 200px;
    margin-bottom: 6rem; /* Further increase margin for very small screens */
  }
}
</style>
