<template>
  <section id="home" class="hero">
    <div class="hero-content">
      <h1 class="hero-title">Welcome to My Portfolio</h1>
      <p class="hero-subtitle">Full Stack Developer | Problem Solver | Creative Thinker</p>
      <div class="hero-buttons">
        <a href="#projects" class="btn btn-primary">View My Work</a>
        <a href="#contact" class="btn btn-secondary">Get In Touch</a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Hero'
}
</script>

<style scoped>
.hero {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  text-align: center;
  padding: 6rem 2rem;
  min-height: 60vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

.hero-content {
  max-width: 800px;
}

.hero-title {
  font-size: 3rem;
  margin-bottom: 1rem;
  animation: fadeInUp 1s ease;
}

.hero-subtitle {
  font-size: 1.5rem;
  margin-bottom: 2rem;
  opacity: 0.9;
  animation: fadeInUp 1s ease 0.2s backwards;
}

.hero-buttons {
  display: flex;
  gap: 1rem;
  justify-content: center;
  animation: fadeInUp 1s ease 0.4s backwards;
}

.btn {
  padding: 0.8rem 2rem;
  border-radius: 5px;
  font-size: 1rem;
  font-weight: 600;
  transition: all 0.3s ease;
  display: inline-block;
  position: relative;
  overflow: hidden;
}

.btn::before {
  content: '';
  position: absolute;
  top: 50%;
  left: 50%;
  width: 0;
  height: 0;
  border-radius: 50%;
  background: rgba(255, 255, 255, 0.3);
  transform: translate(-50%, -50%);
  transition: width 0.6s, height 0.6s;
}

.btn:hover::before {
  width: 300px;
  height: 300px;
}

.btn-primary {
  background: white;
  color: #667eea;
}

.btn-primary:hover {
  transform: translateY(-3px) scale(1.05);
  box-shadow: 0 8px 20px rgba(0,0,0,0.3);
  text-decoration: none;
  animation: pulse 0.6s ease;
}

.btn-primary:active {
  transform: translateY(-1px) scale(1.02);
  box-shadow: 0 3px 10px rgba(0,0,0,0.2);
}

.btn-secondary {
  background: transparent;
  color: white;
  border: 2px solid white;
}

.btn-secondary::before {
  background: rgba(255, 255, 255, 0.15);
}

.btn-secondary:hover {
  background: white;
  color: #667eea;
  text-decoration: none;
  transform: translateY(-3px) scale(1.05);
  box-shadow: 0 8px 20px rgba(255,255,255,0.3);
  animation: pulse 0.6s ease;
}

.btn-secondary:active {
  transform: translateY(-1px) scale(1.02);
  box-shadow: 0 3px 10px rgba(255,255,255,0.2);
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes pulse {
  0%, 100% {
    transform: translateY(-3px) scale(1.05);
  }
  50% {
    transform: translateY(-3px) scale(1.08);
  }
}

@media (max-width: 768px) {
  .hero-title {
    font-size: 2rem;
  }
  
  .hero-subtitle {
    font-size: 1.2rem;
  }
  
  .hero-buttons {
    flex-direction: column;
    align-items: center;
  }
  
  .btn {
    width: 100%;
    max-width: 250px;
  }
}
</style>
