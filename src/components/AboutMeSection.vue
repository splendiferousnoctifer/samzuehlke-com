<!-- src/components/AboutMeSection.vue -->
<template>
    <div class="about-me-section">
      <div class="content">
        <div class="heading">
          <h2 id="about">(About Me)</h2>
        </div>
        <div class="text">
            <p>
                I'm a research associate at the <b>Digital Media Lab</b> and a part-time lecturer. My work focuses on textile sensors, Interaction Design, LLM applications, and various machine learning projects. My research interests span Computer Vision, Machine Learning, and Textile Sensors, with a particular passion for Data Science, Immersive and Generative Arts, Brain-Computer Interfaces, and Accessibility and Adaptability for Neurodiverse People. I consider myself a multi-hyphenate IT and media generalist, with a diverse background in Computer Science and UI/UX Design.
            </p>
        </div>
      </div>
      <hr class="section-divider" />
    </div>
  </template>
  
  <script lang="ts">
  export default {
    name: 'AboutMeSection'
  }
  </script>
  
  <style scoped>
  .about-me-section {
    width: 60vw; /* Same width as the other components */
    margin: 0 auto; /* Center the component horizontally */
    padding: 50px 20px 0 20px; /* Padding above and below the section */
    box-sizing: border-box; /* Include padding in the element's total width */
  }
  
  .content {
    display: flex; /* Use flexbox to align items horizontally */
    align-items: flex-start; /* Align items at the top */
    gap: 20px; /* Space between items */
  }
  
  .heading {
    display: flex;
    align-items: center;
    padding-right: 50px; /* Padding to the right of the heading */
  }
  
  h2 {
    font-size: 1.25rem; /* Font size for the heading */
    color: black; /* Set text color to black */
    margin: 0; /* Remove default margin */
  }
  
  .text {
    flex: 1; /* Allow text to take remaining space */
  }
  
  .text p {
    font-size: 1rem; /* Font size for the paragraph */
    line-height: 1.6; /* Line spacing for readability */
    margin: 0;
    padding-left: 50px; /* Padding for space between text and border */
    border-left: 2px solid black; /* Left border for separation */
    text-align: justify; /* Justify text to align both left and right */
    text-align-last: left; /* Align the last line of text to the left */
  }

  /* Horizontal line styling */
.section-divider {
  border: none; /* Remove default border */
  border-top: 2px solid black; /* Black line with a thickness of 2px */
  margin: 40px 0; /* Space above and below the line */
  width: 100%; /* Full width of the container */
}
  </style>
  