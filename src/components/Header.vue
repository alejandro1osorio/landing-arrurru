<template>
    <header class="header">
      <h1>Header Component</h1>
      <nav>
        <ul>
          <li><a href="#">Home</a></li>
          <li><a href="#">About</a></li>
          <li><a href="#">Contact</a></li>
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
    background-color: #4CAF50;
    color: white;
    padding: 1em;
    text-align: center;
  }
  .header ul {
    list-style-type: none;
    padding: 0;
  }
  .header li {
    display: inline;
    margin: 0 10px;
  }
  .header a {
    color: white;
    text-decoration: none;
  }
  </style>
  