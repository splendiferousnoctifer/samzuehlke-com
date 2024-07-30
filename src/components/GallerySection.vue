<template>
    <div class="gallery-section">
        <div class="heading">
            <h1 id="publications">Publications</h1>
        </div>
      <div class="gallery-container">
        <div class="gallery-box" @click="navigateTo('https://example.com/link1')">
          <div class="date">July 2023</div>
          <img src="/test.jpg" alt="Image 1" class="image"/>
          <div class="title">Title 1</div>
          <div class="authors">Author 1, Author 2</div>
        </div>
        <div class="gallery-box" @click="navigateTo('https://example.com/link2')">
          <div class="date">August 2023</div>
          <img src="/test.jpg" alt="Image 2" class="image"/>
          <div class="title">Title 2</div>
          <div class="authors">Author 3, Author 4</div>
        </div>
        <div class="gallery-box" @click="navigateTo('https://example.com/link3')">
          <div class="date">September 2023</div>
          <img src="/test.jpg" alt="Image 3" class="image"/>
          <div class="title">Title 3</div>
          <div class="authors">Author 5, Author 6</div>
        </div>
      </div>
      <hr class="section-divider" />

    </div>
  </template>
  
  <script lang="ts">
  export default {
    name: 'GallerySection',
    methods: {
      navigateTo(url: string) {
        window.location.href = url;
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
  