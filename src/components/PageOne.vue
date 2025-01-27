<template>
  <div class="page-content">
    <div class="header">
      <h1 class="title">Crema <span class="highlight">Recién Nacido</span></h1>
    </div>
    <div class="center-container">
      <img src="../assets/productos/crema.png" alt="Crema Recien Nacido" class="center-image" />
    </div>
  </div>
</template>

<script>
export default {
  name: "PageOne",
};
</script>

<style scoped>
.page-content {
  width: 90%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  box-sizing: border-box;
  text-align: center;
  margin: 0 auto;
}

.header {
  margin-bottom: 20px;
}

.title {
  font-size: 1.8rem;
  color: #333;
}

.highlight {
  color: #007bff;
}

.center-container {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 80%;
  max-width: 400px;
  height: 10%;
  margin: 0 auto;
  padding: 15px;
  background-color: #f9f9f9;
  border-radius: 10px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.center-image {
  max-width: 100%;
  height: 40%;
  border-radius: 10px;
}

@media (max-width: 768px) {
  .title {
    font-size: 1.5rem;
  }

  .center-container {
    padding: 10px;
    max-width: 300px;
  }
}
</style>
