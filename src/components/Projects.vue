<template>
  <section id="projects" class="projects">
    <h2>My Projects</h2>
    <div class="project-grid">
      <div class="project-card" v-for="project in projects" :key="project.id">
        <h3>{{ project.title }}</h3>
        <p>{{ project.description }}</p>
        <div class="project-tags">
          <span class="tag" v-for="tag in project.tags" :key="tag">{{ tag }}</span>
        </div>
        <a :href="project.link" class="project-link" target="_blank" rel="noopener">View Project →</a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Projects',
  data() {
    return {
      projects: [
        {
          id: 1,
          title: 'E-Commerce Platform',
          description: 'A full-featured e-commerce platform with shopping cart, payment integration, and admin dashboard.',
          tags: ['Vue.js', 'Node.js', 'MongoDB'],
          link: '#'
        },
        {
          id: 2,
          title: 'Task Management App',
          description: 'A collaborative task management application with real-time updates and team features.',
          tags: ['Vue.js', 'Firebase', 'Tailwind'],
          link: '#'
        },
        {
          id: 3,
          title: 'Weather Dashboard',
          description: 'A beautiful weather dashboard that displays current conditions and forecasts for multiple cities.',
          tags: ['Vue.js', 'API', 'Charts'],
          link: '#'
        },
        {
          id: 4,
          title: 'Portfolio Website',
          description: 'A modern, responsive portfolio website built with Vue.js and Vite.',
          tags: ['Vue.js', 'Vite', 'CSS'],
          link: '#'
        }
      ]
    }
  }
}
</script>

<style scoped>
.projects {
  background: white;
}

.projects h2 {
  text-align: center;
  font-size: 2.5rem;
  color: #2c3e50;
  margin-bottom: 3rem;
}

.project-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2rem;
}

.project-card {
  background: #f8f9fa;
  padding: 2rem;
  border-radius: 10px;
  box-shadow: 0 2px 10px rgba(0,0,0,0.1);
  transition: transform 0.3s, box-shadow 0.3s;
  display: flex;
  flex-direction: column;
}

.project-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 5px 20px rgba(0,0,0,0.15);
}

.project-card h3 {
  color: #2c3e50;
  font-size: 1.5rem;
  margin-bottom: 1rem;
}

.project-card p {
  color: #555;
  line-height: 1.6;
  flex: 1;
  margin-bottom: 1rem;
}

.project-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  margin-bottom: 1rem;
}

.tag {
  background: #667eea;
  color: white;
  padding: 0.3rem 0.8rem;
  border-radius: 20px;
  font-size: 0.85rem;
  font-weight: 500;
}

.project-link {
  color: #667eea;
  font-weight: 600;
  align-self: flex-start;
  transition: color 0.3s;
}

.project-link:hover {
  color: #764ba2;
}
</style>
