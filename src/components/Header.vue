<template>
  <header>
    <nav>
      <div class="logo">
        <h2>My Portfolio</h2>
      </div>
      <ul class="nav-links">
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
      <a href="https://github.com/ihilley74-sudo/https-github.com-ian7306-vuemy_project.git-" 
         target="_blank" 
         rel="noopener noreferrer" 
         class="fork-button">
        Fork on GitHub
      </a>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style scoped>
header {
  background: #2c3e50;
  color: white;
  padding: 1rem 2rem;
  position: sticky;
  top: 0;
  z-index: 100;
  box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}

nav {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo h2 {
  margin: 0;
  font-size: 1.5rem;
}

.nav-links {
  display: flex;
  list-style: none;
  gap: 2rem;
}

.nav-links a {
  color: white;
  font-weight: 500;
  transition: color 0.3s;
}

.nav-links a:hover {
  color: #4a90e2;
  text-decoration: none;
}

.fork-button {
  background: #4a90e2;
  color: white;
  padding: 0.5rem 1rem;
  border-radius: 5px;
  font-weight: 500;
  transition: all 0.3s ease;
  border: 2px solid #4a90e2;
}

.fork-button:hover {
  background: #357abd;
  border-color: #357abd;
  text-decoration: none;
  transform: translateY(-2px);
  box-shadow: 0 4px 8px rgba(0,0,0,0.2);
}

@media (max-width: 768px) {
  nav {
    flex-direction: column;
    gap: 1rem;
  }
  
  .nav-links {
    gap: 1rem;
  }
}
</style>
