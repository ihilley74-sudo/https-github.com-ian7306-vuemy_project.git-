<template>
  <section id="about" class="about">
    <h2>About Me</h2>
    <div class="about-content">
      <div class="about-text">
        <p>
          Hello! I'm a passionate developer with a love for creating beautiful and functional web applications.
          I specialize in modern web technologies and enjoy turning complex problems into simple, elegant solutions.
        </p>
        <p>
          With experience in both front-end and back-end development, I bring a comprehensive understanding
          of the full development lifecycle. I'm always eager to learn new technologies and best practices.
        </p>
      </div>
      <div class="skills">
        <h3>Skills</h3>
        <div class="skill-grid">
          <div class="skill-item">Vue.js</div>
          <div class="skill-item">JavaScript</div>
          <div class="skill-item">HTML/CSS</div>
          <div class="skill-item">Node.js</div>
          <div class="skill-item">Git</div>
          <div class="skill-item">Responsive Design</div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'About'
}
</script>

<style scoped>
.about {
  background: #f8f9fa;
}

.about h2 {
  text-align: center;
  font-size: 2.5rem;
  color: #2c3e50;
  margin-bottom: 2rem;
}

.about-content {
  display: grid;
  gap: 3rem;
}

.about-text p {
  font-size: 1.1rem;
  line-height: 1.8;
  margin-bottom: 1rem;
  color: #555;
}

.skills h3 {
  font-size: 1.8rem;
  color: #2c3e50;
  margin-bottom: 1.5rem;
}

.skill-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  gap: 1rem;
}

.skill-item {
  background: white;
  padding: 1rem;
  border-radius: 8px;
  text-align: center;
  font-weight: 600;
  color: #667eea;
  box-shadow: 0 2px 5px rgba(0,0,0,0.1);
  transition: transform 0.3s, box-shadow 0.3s;
}

.skill-item:hover {
  transform: translateY(-5px);
  box-shadow: 0 5px 15px rgba(0,0,0,0.2);
}

@media (min-width: 768px) {
  .about-content {
    grid-template-columns: 1fr 1fr;
  }
}
</style>
