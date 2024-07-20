<template>
  <div class="image-section" ref="imageSection">
    <img src="/test.jpg" alt="Decorative Image" class="image" ref="image" />
  </div>
</template>

<script lang="ts">
import { defineComponent, ref, onMounted, onUnmounted, computed } from 'vue';

export default defineComponent({
  setup() {
    const imageSection = ref<HTMLDivElement | null>(null);
    const image = ref<HTMLImageElement | null>(null);

    const handleScroll = () => {
      if (imageSection.value) {
        const sectionHeight = imageSection.value.offsetHeight;
        const scrollY = window.scrollY;
        const maxScroll = document.documentElement.scrollHeight - window.innerHeight;
        const scrollPercent = Math.min(scrollY / maxScroll, 1);
        const zoom = 1 + (0.2 * scrollPercent);

        if (image.value) {
          image.value.style.transform = `scale(${zoom})`;
        }
      }
    };

    onMounted(() => {
      window.addEventListener('scroll', handleScroll);
      handleScroll(); // Initialize the zoom on mount
    });

    onUnmounted(() => {
      window.removeEventListener('scroll', handleScroll);
    });

    return {
      imageSection,
      image
    };
  }
});
</script>

<style scoped>
.image-section {
  width: 60vw;
  height: 33.75vw;
  overflow: hidden;
  position: relative;
  border: 1px solid #ddd; /* Optional for better visibility */
}

.image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.2s; /* Smooth zoom transition */
}
</style>
