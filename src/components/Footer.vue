<template>
  <footer>
    <div class="footer-content">
      <p>&copy; {{ currentYear }} My Portfolio. All rights reserved.</p>
      <p>Built with Vue.js and ❤️</p>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  computed: {
    currentYear() {
      return new Date().getFullYear()
    }
  }
}
</script>

<style scoped>
footer {
  background: #2c3e50;
  color: white;
  text-align: center;
  padding: 2rem;
  margin-top: auto;
}

.footer-content p {
  margin: 0.5rem 0;
  opacity: 0.9;
}
</style>
