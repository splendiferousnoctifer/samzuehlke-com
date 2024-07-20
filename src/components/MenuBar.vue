<!-- src/components/MenuBar.vue -->
<template>
  <div class="menu-bar">
    <nav>
      <ul>
        <li><a href="#top">Home</a></li> <!-- Adjusted href for Home -->
        <li><a href="#about">About</a></li>
        <li><a href="#cv">Resume</a></li>
        <li><a href="#publications">Publications</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </div>
</template>

<script lang="ts">
export default {
name: 'MenuBar'
}
</script>

<style scoped>
.menu-bar {
width: 60vw; /* 60% of the viewport width */
/*border-bottom: 2px solid rgb(0, 0, 0); /* Black border only on the bottom */
background-color: var(--color-background);
box-shadow: none; /* No shadow */
padding: 20px 20px; /* Padding underneath the menu bar */
box-sizing: border-box; /* Ensure padding and border are included in the width */
position: fixed; /* Fix the menu bar in place */
top: 0; /* Stick to the top of the viewport */
left: 50%; /* Center it horizontally */
transform: translateX(-50%); /* Adjust for centering */
z-index: 1000; /* Ensure the menu bar stays above other content */
}

nav ul {
list-style: none;
padding: 0;
margin: 0;
display: flex;
justify-content: flex-end; /* Right-align the items */
width: 100%;
}

nav ul li {
margin: 0;
}

nav ul li a {
text-decoration: none;
color: var(--color-text);
font-weight: 500;
padding: 15px 20px; /* Add some padding for better click area */
}

nav ul li a:hover {
text-decoration: underline;
}
</style>
