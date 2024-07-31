<template>
  <div class="menu-bar">
    <nav>
      <ul>
        <li><a href="#top" @click.prevent="scrollToTop">Home</a></li>
        <li><a href="#about" @click.prevent="scrollToSection('about')">About</a></li>
        <li><a href="#publications" @click.prevent="scrollToSection('publications')">Publications</a></li>
        <li><a href="#cv" @click.prevent="scrollToSection('cv')">Resume</a></li>
        <li><a href="#contact" @click.prevent="scrollToSection('contact')">Contact</a></li>
      </ul>
    </nav>
  </div>
</template>

<script lang="ts">
export default {
  name: 'MenuBar',
  methods: {
    scrollToTop() {
      window.scrollTo({
        top: 0,
        behavior: 'smooth'
      });
    },
    scrollToSection(id: string) {
      const element = document.getElementById(id);
      if (element) {
        // Calculate the offset to center the element vertically
        const viewportHeight = window.innerHeight;
        const elementHeight = element.offsetHeight;
        const offset = (viewportHeight - elementHeight) / 2;
        window.scrollTo({
          top: element.offsetTop - offset,
          behavior: 'smooth'
        });
      }
    }
  }
}
</script>

<style scoped>
.menu-bar {
  width: 60vw; /* 60% of the viewport width */
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
