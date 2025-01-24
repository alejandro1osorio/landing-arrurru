<template>
  <header class="header">
    <img src="../assets/logos-sellos/logo-arrurru.png" alt="Logo" class="header-logo" />
    <nav class="header-nav">
      <ul class="nav-list">
        <li class="nav-item">
          <a href="#" class="nav-link active">Inicio</a>
        </li>
        <li class="nav-item">
          <a href="#" class="nav-link">Baño</a>
        </li>
        <li class="nav-item">
          <a href="#" class="nav-link">Masaje</a>
        </li>
        <li class="nav-item">
          <a href="#" class="nav-link">Cuidado de la Colita</a>
        </li>
        <li class="nav-item">
          <a href="#" class="nav-link">Preguntas Frecuentes</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped>
.header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1rem 2rem; /* Uniform padding for consistent spacing */
  position: absolute;
  top: 0;
  width: 100%;
  background-color: transparent; /* Transparent header */
  z-index: 10;
}

.header-logo {
  width: 150px;
  height: auto;
  margin-left: 2rem; /* Add left margin to separate from the edge */
}

.header-nav {
  flex-grow: 1;
  display: flex;
  justify-content: flex-end;
  padding-right: 2rem; /* Add right padding to the navigation */
  position: fixed;
  right: 0;
}

.nav-list {
  display: flex;
  gap: 1.5rem;
  list-style: none;
  margin: 0;
  padding: 0.8rem 2rem;
  background-color: rgba(255, 255, 255, 0.8);
  border-radius: 20px;
}

.nav-item {
  text-align: center;
}

.nav-link {
  text-decoration: none;
  color: #214F79;
  font-weight: 400;
  position: relative;
  transition: color 0.3s ease;
}

.nav-link::after {
  content: "";
  display: block;
  width: 0;
  height: 2px;
  background-color: #a70c55;
  margin: 0 auto;
  transition: width 0.3s ease;
}

.nav-link:hover::after,
.nav-link.active::after {
  width: 50%;
}

.nav-link.active {
  font-weight: bold;
  color: #214F79;
}

.nav-link:hover {
  font-weight: bold;
  color: #214F79;
}

@media (max-width: 768px) {
  .header-logo {
    display: none;
  }

  .nav-list {
    justify-content: center;
  }
}
</style>
