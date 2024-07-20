<!-- src/components/IntroSection.vue -->
<template>
    <div class="intro-section">
      <div class="intro">
        <h1>
          Samuel Zühlke <br />
          BSc MSc       
        </h1>
        <p class="location">(Linz, Austria)</p> <!-- Added location text -->
      </div>
      <div class="scroll-down">
        <button class="scroll-button">
          Scroll Down
          <span class="arrow material-symbols-outlined">south_east</span> <!-- Use Material Symbols -->
        </button>
      </div>
    </div>
  </template>
  
  <script lang="ts">
  export default {
    name: 'IntroSection'
  }
  </script>
  
  <style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@20..48,100..700,0..1,-50..200');
  
  .intro-section {
    display: grid;
    grid-template-columns: 1fr 4fr 1fr; /* 7 columns: with empty left and right columns */
    grid-template-rows: auto; /* Single row */
    gap: 40px; /* Increased gap between sections */
    padding-bottom: 20px; /* Padding inside the section */
    padding-top: 40px;
  }
  
  .intro {
    grid-column: 1 / span 4; /* Spans columns 1 to 4 */
    display: flex;
    flex-direction: column;
    align-items: flex-start; /* Left-align the name */
    padding-left: 0; /* Align with grid columns */
  }
  
  .intro h1 {
    font-size: 4.5rem; /* Larger font size for the name */
    font-weight: bold;
    color: black; /* Set text color to black */
    margin: 0; /* Remove default margin */
    line-height: 1.1; /* Reduce line spacing */
  }
  
  .intro .location {
    font-size: 1.25rem; /* Smaller font size for location */
    color: black; /* Set text color to black */
    margin: 0; /* Remove default margin */
    margin-top: 0.5rem; /* Add some space above the location text */
  }
  
  .scroll-down {
    grid-column: 6; /* Column 6 */
    display: flex;
    align-items: flex-end; /* Align to the bottom */
    justify-content: flex-end; /* Align to the right */
    padding-right: 0.5rem; /* Padding from the right */
    padding-bottom: 0.5rem; /* Padding from the bottom */
  }
  
  .scroll-button {
    background-color: black;
    color: white;
    border: none;
    border-radius: 25px; /* Rounded edges */
    padding: 10px 20px;
    font-size: 1rem;
    font-weight: 500;
    display: flex;
    align-items: center;
    gap: 10px; /* Space between text and arrow */
    transition: background-color 0.3s, transform 0.3s;
  }
  

  .arrow {
    font-size: 1.5rem; /* Adjust arrow size */
    display: inline-block;
    font-family: 'Material Symbols Outlined'; /* Use Material Symbols Outlined font */
  }
  </style>
  