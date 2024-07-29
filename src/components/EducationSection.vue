<template>
  <div class="education-section">
    <div class="heading">
      <h1 id="education">Education</h1>
    </div>
    <div class="education-content">
      <table class="education-table">
        <colgroup>
          <col class="column-details" />
          <col class="column-description" />
        </colgroup>
        <tbody>
          <tr>
            <td class="education-details">
              <div class="timeframe">October 2021 – July 2023</div>
              <div class="job-position">Interactive Media</div>
              <div class="employer">FH Hagenberg</div>
            </td>
            <td class="education-description">
              <div>Master's Degree - Passed with highest Distinction</div>
              <div>Thesis: "Touch Sensing on Semi-Elastic Textiles with Border-Based Sensors"</div>
            </td>
          </tr>
          <tr>
            <td class="education-details">
              <div class="timeframe">October 2018 – July 2021</div>
              <div class="job-position">Mediatechnology and -design</div>
              <div class="employer">FH Hagenberg</div>
            </td>
            <td class="education-description">
              <div>Bachelor's Degree - Passed with highest Distinction</div>
              <div>Thesis: "Conception and Creation of a Handheld Text Input Device and its System of Operation"</div>
            </td>
          </tr>
       
        </tbody>
      </table>
    </div>
    <div class="education-actions">
      <a href="/path-to-education.pdf" class="education-button">Download resume PDF</a>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  name: 'educationSection'
}
</script>

<style scoped>
.education-section {
  width: 60vw; /* Same width as the other components */
  margin: 0 auto; /* Center the component horizontally */
  padding-right: 20px; /* Padding on the right */
  box-sizing: border-box; /* Include padding in the element's total width */
}

.heading {
  margin-left: 20px; /* Match the indentation of the intro section */
}

h1 {
  font-size: 3rem; /* Larger font size for the heading */
  font-weight: bold;
  color: black; /* Set text color to black */
  margin: 0; /* Remove default margin */
  line-height: 1.1; /* Reduce line spacing */
}

.education-content {
  padding: 20px 0;
}

.education-table {
  width: 100%;
  border-collapse: collapse; /* Collapse borders for table */
  table-layout: fixed; /* Fix column widths */
  margin: 20px;
  padding-right: 20px;
}

.education-table colgroup {
  display: table-column-group;
}

.education-table col.column-details {
  width: 33%; /* 1/3 of the table width */
}

.education-table col.column-description {
  width: 67%; /* 2/3 of the table width */
}

.education-table td {
  vertical-align: top; /* Align text at the top */
  padding-top: 10px;
  padding-bottom: 10px;
  padding-right: 20px;
  border-bottom: 1px solid black; /* Horizontal lines between rows */
}

.education-table tr:last-child td {
  border-bottom: none; /* Remove the bottom border of the last row */
}

.education-details {
  /* No vertical line styling */
}

.education-details .timeframe,
.education-details .job-position,
.education-details .employer {
  font-size: 0.875rem; /* Smaller font size for dates */
  text-align: justify; /* Justify text alignment */
}

.education-details .job-position {
  font-size: 1.5rem; /* Larger font size for job positions */
  font-weight: bold; /* Bold font for job positions */
}

.education-details .employer {
  font-size: 1rem; /* Medium font size for employer names */
  text-align: justify; /* Justify text alignment */
}

.education-description {
  font-size: 1rem; /* Regular font size for descriptions */
  text-align: justify; /* Justify text alignment */
}

.education-actions {
  display: flex;
  justify-content: flex-start; /* Align button to the left */
  padding-top: 20px; /* Space above the button */
}

.education-button {
  background-color: black; /* Button background color */
  color: white; /* Button text color */
  text-decoration: none; /* Remove underline */
  padding: 10px 20px; /* Padding inside the button */
  border-radius: 25px; /* Rounded corners */
  font-size: 1rem; /* Font size */
  font-weight: 500; /* Font weight */
  display: flex;
  align-items: center;
  gap: 10px; /* Space between text and icon if needed */
  cursor: pointer;
  transition: none; /* No transition effects */
  margin-left: 20px;
}

.education-button:hover {
  background-color: black; /* Maintain background color on hover */
  color: white; /* Maintain text color on hover */
}
</style>
