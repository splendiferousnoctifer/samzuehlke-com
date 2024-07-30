<!-- src/components/MainContent.vue -->
<template>
    <main class="main-content">
      
  
      <section id="contact" class="content-section">
        <h2>Contact</h2>
        <p>This is the contact section.</p>
      </section>
    </main>
  </template>
  
  <script lang="ts">
  export default {
    name: 'MainContent'
  }
  </script>
  
  <style scoped>
  .main-content {
    grid-column: 1 / span 7; /* Span across all columns */
    grid-row: 3; /* Third row */
    padding: 20px; /* Adjust padding if needed */
  }
  
  .content-section {
    margin-bottom: 40px; /* Space between sections */
  }
  
  h1, h2 {
    margin-top: 0;
  }
  </style>
  