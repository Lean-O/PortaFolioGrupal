<script setup>
import { ref } from 'vue'

const skills = ref([
  { name: 'Autopsy Digital Forensics', img: '/public/Leanjua/Autopsy Digital Forensics.png' },
  { name: 'AWS', img: '/public/Leanjua/aws.png' },
  { name: 'Cisco', img: '/public/Leanjua/cisco.png' },
  { name: 'C#', img: '/public/Leanjua/csharp.png' },
  { name: 'CSS', img: '/public/Leanjua/css.png' },
  { name: 'Docker', img: '/public/Leanjua/docker.png' },
  { name: 'Express', img: '/public/Leanjua/express.png' },
  { name: 'Flutter', img: '/public/Leanjua/flutter.png' },
  { name: 'GraphQL', img: '/public/Leanjua/graphql.png' },
  { name: 'HTML', img: '/public/Leanjua/html.png' },
  { name: 'Java', img: '/public/Leanjua/java.png' },
  { name: 'JavaScript', img: '/public/Leanjua/Js.png' },
  { name: 'Kali Linux', img: '/public/Leanjua/Kali, Linux.png' },
  { name: 'TypeScript', img: '/public/Leanjua/mecanografiado.png' },
  { name: 'MongoDB', img: '/public/Leanjua/mongodb.png' },
  { name: 'MySQL', img: '/public/Leanjua/mysql.png' },
  { name: 'Node.js', img: '/public/Leanjua/nodejs.png' },
  { name: 'OrangeWhile', img: '/public/Leanjua/orangewhile.png' },
  { name: 'Python', img: '/public/Leanjua/piton.png' },
  { name: 'PostgreSQL', img: '/public/Leanjua/postgresql.png' },
  { name: 'React', img: '/public/Leanjua/react_.png' },
  { name: 'Red Hat', img: '/public/Leanjua/redhat_.png' },
  { name: 'Tailwind CSS', img: '/public/Leanjua/tailwindcss.png' },
  { name: 'Visual Studio', img: '/public/Leanjua/visual-basico.png' },
  { name: 'Vue.js', img: '/public/Leanjua/vuejs.png' }
])
</script>

<template>
  <div class="habilidades-section">
    <div class="habilidades-container">
      <h2 class="section-title">Tecnologías</h2>
      <div class="skills-container">
        <div
          v-for="(skill, index) in skills"
          :key="index"
          class="skill-card"
        >
          <img 
            :src="skill.img" 
            :alt="skill.name"
            class="skill-icon"
          />
          <span class="skill-name">{{ skill.name }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.habilidades-section {
  min-height: 100vh;
  padding: 5rem 1rem;
}

.habilidades-container {
  max-width: 80rem;
  margin: 0 auto;
}

.section-title {
  font-size: 3rem;
  font-weight: 700;
  text-align: center;
  margin-bottom: 4rem;
  background: linear-gradient(to right, #06b6d4, #a855f7);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.skills-container {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(140px, 1fr));
  gap: 2rem;
  justify-items: center;
}

.skill-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 1rem;
  padding: 1.5rem;
  background: rgba(15, 23, 42, 0.5);
  backdrop-filter: blur(20px);
  border-radius: 1rem;
  border: 1px solid #1e293b;
  transition: all 0.3s;
  cursor: pointer;
  width: 140px;
  height: 140px;
}

.skill-card:hover {
  transform: translateY(-8px) scale(1.05);
  border-color: rgba(6, 182, 212, 0.5);
  box-shadow: 0 8px 32px rgba(6, 182, 212, 0.2);
}

.skill-icon {
  width: 60px;
  height: 60px;
  object-fit: contain;
  transition: transform 0.3s;
}

.skill-card:hover .skill-icon {
  transform: scale(1.1);
}

.skill-name {
  font-size: 0.75rem;
  color: #cbd5e1;
  text-align: center;
  font-weight: 500;
}

@media (max-width: 768px) {
  .section-title {
    font-size: 2rem;
  }
  
  .skills-container {
    grid-template-columns: repeat(auto-fill, minmax(110px, 1fr));
    gap: 1.5rem;
  }
  
  .skill-card {
    width: 110px;
    height: 110px;
    padding: 1rem;
  }
  
  .skill-icon {
    width: 50px;
    height: 50px;
  }
  
  .skill-name {
    font-size: 0.65rem;
  }
}
</style>