<template>
    <div class="gallery-section">
        <div class="heading">
            <h1>Publications</h1>
        </div>
      <div id="publications" class="gallery-container">
        <div class="gallery-box" @click="navigateTo('https://doi.org/10.1145/3641234.3671083')">
          <div class="date">July 2024 - SIGGRAPH24</div>
          <img src="https://dl.acm.org/cms/attachment/html/10.1145/3641234.3671083/assets/html/images/siggraphposters24-66-fig1.jpg" alt="Image 1" class="image"/>
          <div class="title">TexEdge: Towards an Approach for Optimization of Sensor Layouts in Textile Interfaces</div>
          <div class="authors">Samuel Zühlke; Sara Mlakar; Kathrin Probst; David C. Schedl</div>
        </div>
        <div class="gallery-box" @click="navigateTo('https://doi.org/10.1145/3643834.3661531')">
          <div class="date">July 2024 - DIS24</div>
          <img src="https://dl.acm.org/cms/attachment/html/10.1145/3643834.3661531/assets/html/images/dis24-119-fig1.jpg" alt="Image 2" class="image"/>
          <div class="title">Threads of Traceability: Textile IDs in the Fabric of Sustainable Fashion
          </div>
          <div class="authors"> Mira Alida Haberfellner*; Samuel Zühlke*; Leopold Boess; Kathrin Probst; Michael Haller</div>
        </div>
        <div class="gallery-box" @click="navigateTo('https://doi.org/10.54941/ahfe1004144')">
          <div class="date">September 2023 - IHSED23</div>
          <img src="https://www.researchgate.net/profile/Samuel-Zuehlke/publication/372462589/figure/fig1/AS:11431281218979264@1705862073340/Comparison-of-the-mathematical-model-to-real-world-measurements-The-RMS-of-the.ppm" alt="Image 3" class="image"/>
          <div class="title">Touch Sensing on Semi-Elastic Textiles with Border-Based Sensors</div>
          <div class="authors">Samuel Zühlke; Andreas Stöckl; David Schedl</div>
        </div>
      </div>
      <hr class="section-divider" />

    </div>
  </template>
  
  <script lang="ts">
  export default {
    name: 'GallerySection',
    methods: {
      /**
       * Navigate to the specified URL in new tab
       * @param url The URL to navigate to
       */
      navigateTo(url: string) {
        const newWindow = window.open(url, '_blank');
        if (newWindow) {
          newWindow.focus();
        }
      }
    }
  }
  </script>
  
  <style scoped>
  .gallery-section {
    width: 60vw; /* Same width as the other components */
    margin: 0 auto; /* Center the component horizontally */
    padding-left: 20px;
    padding-right: 20px;
    box-sizing: border-box; /* Include padding in the element's total width */
  }
  
  .gallery-container {
    display: flex; /* Display boxes side by side */
    gap: 10px; /* Space between boxes */
  }
  
  .gallery-box {
    width: 33.33%; /* Each box takes up one-third of the width */
    border: 2px solid black; /* Black border around each box */
    box-sizing: border-box; /* Include padding and border in the element's total width */
    padding: 10px; /* Padding inside the box */
    cursor: pointer; /* Change cursor to pointer on hover */
    transition: background-color 0.3s; /* Smooth transition for background color */
  }
  
  .gallery-box:hover {
    background-color: #f0f0f0; /* Light background color on hover */
  }
  
  .date {
    font-size: 0.875rem; /* Smaller font size for date */
    color: black; /* Black text color */
    margin-bottom: 10px; /* Space below the date */
  }
  
  .image {
    width: 100%; /* Image width as wide as the box */
    height: auto; /* Maintain aspect ratio */
    margin-bottom: 10px; /* Space below the image */
  }
  
  .title {
    font-size: 1.25rem; /* Larger font size for title */
    font-weight: bold; /* Bold font for title */
    margin-bottom: 5px; /* Space below the title */
  }
  
  .authors {
    font-size: 0.875rem; /* Smaller font size for authors */
    color: #555; /* Grey text color for authors */
  }

  .heading {
    margin-bottom: 20px;
  }

  h1 {
    font-size: 3rem; /* Larger font size for the heading */
    font-weight: bold;
    color: black; /* Set text color to black */
    margin: 0; /* Remove default margin */
    line-height: 1.1; /* Reduce line spacing */
  }

    .section-divider {
  border: none; /* Remove default border */
  border-top: 2px solid black; /* Black line with a thickness of 2px */
  margin: 40px 0; /* Space above and below the line */
  width: 60wv; /* Full width of the container */
}
  </style>
  