<template>
  <section id="contact" class="contact">
    <h2>Get In Touch</h2>
    <div class="contact-content">
      <div class="contact-info">
        <p>I'm always interested in hearing about new projects and opportunities.</p>
        <div class="contact-methods">
          <div class="contact-method">
            <strong>Email:</strong>
            <a href="mailto:your.email@example.com">your.email@example.com</a>
          </div>
          <div class="contact-method">
            <strong>GitHub:</strong>
            <a href="https://github.com/yourusername" target="_blank" rel="noopener">github.com/yourusername</a>
          </div>
          <div class="contact-method">
            <strong>LinkedIn:</strong>
            <a href="https://linkedin.com/in/yourusername" target="_blank" rel="noopener">linkedin.com/in/yourusername</a>
          </div>
        </div>
      </div>
      <form class="contact-form" @submit.prevent="handleSubmit">
        <div class="form-group">
          <label for="name">Name</label>
          <input type="text" id="name" v-model="form.name" required>
        </div>
        <div class="form-group">
          <label for="email">Email</label>
          <input type="email" id="email" v-model="form.email" required>
        </div>
        <div class="form-group">
          <label for="message">Message</label>
          <textarea id="message" v-model="form.message" rows="5" required></textarea>
        </div>
        <button type="submit" class="submit-btn">Send Message</button>
      </form>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Contact',
  data() {
    return {
      form: {
        name: '',
        email: '',
        message: ''
      }
    }
  },
  methods: {
    handleSubmit() {
      alert(`Thank you ${this.form.name}! Your message has been received.`)
      this.form = { name: '', email: '', message: '' }
    }
  }
}
</script>

<style scoped>
.contact {
  background: #f8f9fa;
}

.contact h2 {
  text-align: center;
  font-size: 2.5rem;
  color: #2c3e50;
  margin-bottom: 2rem;
}

.contact-content {
  display: grid;
  gap: 3rem;
}

.contact-info p {
  font-size: 1.1rem;
  color: #555;
  margin-bottom: 2rem;
}

.contact-methods {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.contact-method {
  display: flex;
  gap: 0.5rem;
  align-items: center;
}

.contact-method strong {
  min-width: 100px;
  color: #2c3e50;
}

.contact-form {
  background: white;
  padding: 2rem;
  border-radius: 10px;
  box-shadow: 0 2px 10px rgba(0,0,0,0.1);
}

.form-group {
  margin-bottom: 1.5rem;
}

.form-group label {
  display: block;
  margin-bottom: 0.5rem;
  color: #2c3e50;
  font-weight: 600;
}

.form-group input,
.form-group textarea {
  width: 100%;
  padding: 0.8rem;
  border: 1px solid #ddd;
  border-radius: 5px;
  font-size: 1rem;
  font-family: inherit;
  transition: border-color 0.3s;
}

.form-group input:focus,
.form-group textarea:focus {
  outline: none;
  border-color: #667eea;
}

.submit-btn {
  background: #667eea;
  color: white;
  padding: 0.8rem 2rem;
  border: none;
  border-radius: 5px;
  font-size: 1rem;
  font-weight: 600;
  cursor: pointer;
  transition: background 0.3s;
}

.submit-btn:hover {
  background: #764ba2;
}

@media (min-width: 768px) {
  .contact-content {
    grid-template-columns: 1fr 1fr;
  }
}
</style>
