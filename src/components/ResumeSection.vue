<template>
  <div class="resume-section">
    <div class="heading">
      <h1 id="resume">Résumé</h1>
    </div>
    <div class="resume-content">
      <table class="resume-table">
        <colgroup>
          <col class="column-details" />
          <col class="column-description" />
        </colgroup>
        <tbody>
          <tr>
            <td class="resume-details">
              <div class="timeframe">July 2022 – Present</div>
              <div class="job-position">Research Associate</div>
              <div class="employer">FH OÖ Research & Development GmbH</div>
            </td>
            <td class="resume-description">
              <div>Digital Media Lab: Engaged in research projects focusing on textile sensors and interaction modalities. Key areas include Computer Vision, Data Science, Machine Learning, and HCI.</div>
              <div>AIST Research Group: Developed LLM applications in the fields of marketing analysis and risk assessment.</div>
            </td>
          </tr>
          <tr>
            <td class="resume-details">
              <div class="timeframe">October 2023 – Present</div>
              <div class="job-position">Lecturer (Part-Time)</div>
              <div class="employer">FH OÖ Studienbetriebs GmbH</div>
            </td>
            <td class="resume-description">
              <div>Conducted and organized courses in Introduction to Programming, Spatial Computing, and Design for Physical Prototyping.</div>
            </td>
          </tr>
          <tr>
            <td class="resume-details">
              <div class="timeframe">March 2021 – September 2022</div>
              <div class="job-position">Digital UI/UX Designer</div>
              <div class="employer">newsadoo GmbH</div>
            </td>
            <td class="resume-description">
              <div>Designed apps and websites. Responsible for UI conception and design, testing, analysis, prototyping, and project management.</div>
              <div>Additional tasks included developing internal graphics, corporate design, and machine learning tasks.</div>
            </td>
          </tr>
          <tr>
            <td class="resume-details">
              <div class="timeframe">December 2020 – May 2021</div>
              <div class="job-position">Graphic Designer</div>
              <div class="employer">Software Competence Center Hagenberg</div>
            </td>
            <td class="resume-description">
              <div>Planned and executed internal corporate design tasks, event design tasks, scientific contributions, and various website designs.</div>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
    <!--
      <div class="resume-actions">
        <a href="/path-to-resume.pdf" class="resume-button">Download Resume PDF</a>
      </div>
      -->
  </div>
</template>

<script lang="ts">
export default {
  name: 'ResumeSection'
}
</script>

<style scoped>
.resume-section {
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

.resume-content {
  padding: 20px 0;
}

.resume-table {
  width: 100%;
  border-collapse: collapse; /* Collapse borders for table */
  table-layout: fixed; /* Fix column widths */
  margin: 20px;
  padding-right: 20px;
}

.resume-table colgroup {
  display: table-column-group;
}

.resume-table col.column-details {
  width: 33%; /* 1/3 of the table width */
}

.resume-table col.column-description {
  width: 67%; /* 2/3 of the table width */
}

.resume-table td {
  vertical-align: top; /* Align text at the top */
  padding-top: 10px;
  padding-bottom: 10px;
  padding-right: 20px;
  border-bottom: 1px solid black; /* Horizontal lines between rows */
}

.resume-table tr:last-child td {
  border-bottom: none; /* Remove the bottom border of the last row */
}

.resume-details {
  /* No vertical line styling */
}

.resume-details .timeframe,
.resume-details .job-position,
.resume-details .employer {
  font-size: 0.875rem; /* Smaller font size for dates */
  text-align: justify; /* Justify text alignment */
}

.resume-details .job-position {
  font-size: 1.5rem; /* Larger font size for job positions */
  font-weight: bold; /* Bold font for job positions */
}

.resume-details .employer {
  font-size: 1rem; /* Medium font size for employer names */
  text-align: justify; /* Justify text alignment */
}

.resume-description {
  font-size: 1rem; /* Regular font size for descriptions */
  text-align: justify; /* Justify text alignment */
}

.resume-actions {
  display: flex;
  justify-content: flex-start; /* Align button to the left */
  padding-top: 20px; /* Space above the button */
}

.resume-button {
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

.resume-button:hover {
  background-color: black; /* Maintain background color on hover */
  color: white; /* Maintain text color on hover */
}
</style>
