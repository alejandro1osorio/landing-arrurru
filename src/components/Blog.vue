<template>
    <div class="blog-container">
      <h1>Artículos Recientes</h1>
      <div class="grid-container">
        <div class="article" v-for="article in articles" :key="article.id">
          <img :src="article.image" alt="Imagen del artículo" class="article-image" />
          <h2>{{ article.title }}</h2>
          <p>{{ article.description }}</p>
          <a href="#" class="view-more">Ver más</a>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "Blog",
    data() {
      return {
        articles: [
          { id: 1, title: "Título 1", description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellendus tempora labore eveniet fuga necessitatibus, quis id. Ratione dolor repudiandae beatae ex veritatis deserunt! Deleniti et, expedita saepe animi est repudiandae accusantium rerum recusandae nulla voluptatibus amet velit beatae quae nisi fuga qui illum. Libero totam ipsam est eos dignissimos voluptatibus quae, omnis illum sunt? Repudiandae perferendis eligendi accusantium numquam id!", image: "https://images.unsplash.com/photo-1461749280684-dccba630e2f6?q=80&w=2069&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" },
          { id: 2, title: "Título 2", description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellendus tempora labore eveniet fuga necessitatibus, quis id. Ratione dolor repudiandae beatae ex veritatis deserunt! Deleniti et, expedita saepe animi est repudiandae accusantium rerum recusandae nulla voluptatibus amet velit beatae quae nisi fuga qui illum. Libero totam ipsam est eos dignissimos voluptatibus quae, omnis illum sunt? Repudiandae perferendis eligendi accusantium numquam id!", image: "https://images.unsplash.com/photo-1646849172022-81577de99470?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" },
          { id: 3, title: "Título 3", description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellendus tempora labore eveniet fuga necessitatibus, quis id. Ratione dolor repudiandae beatae ex veritatis deserunt! Deleniti et, expedita saepe animi est repudiandae accusantium rerum recusandae nulla voluptatibus amet velit beatae quae nisi fuga qui illum. Libero totam ipsam est eos dignissimos voluptatibus quae, omnis illum sunt? Repudiandae perferendis eligendi accusantium numquam id!", image: "https://images.unsplash.com/photo-1659463958698-a6eeccad7e0c?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  .blog-container {
    text-align: center;
    padding: 20px;
  }
  
  h1 {
    font-size: 2.5em;
    color: #2c3e50;
    margin-bottom: 30px;
  }
  
  .grid-container {
    display: grid;
    gap: 20px;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    padding: 10px;
    justify-content: center;
  }
  
  .article {
    background-color: #f9f9f9;
    border-radius: 8px;
    padding: 0;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    text-align: center;
    overflow: hidden;
    padding-bottom: 20px;
  }
  
  .article-image {
    width: 100%;
    height: auto;
    border-radius: 8px 8px 8px 8px;
    margin: 0;
  }
  
  h2 {
    font-size: 1.5em;
    margin: 10px 0;
    color: #34495e;
  }
  
  p {
    font-size: 1em;
    color: #7f8c8d;
    margin: 10px 20px;
    text-align: justify;
  }
  
  .view-more {
    text-decoration: none;
    color: #3498db;
    font-weight: bold;
    transition: color 0.3s;
  }
  
  .view-more:hover {
    color: #1d6fa5;
  }
  
  @media (max-width: 600px) {
    .grid-container {
      grid-template-columns: 1fr;
    }
  }
  </style>
  