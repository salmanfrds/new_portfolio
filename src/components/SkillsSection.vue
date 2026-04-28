<script setup>
const categories = [
  {
    icon: '📱',
    name: 'Mobile',
    skills: ['Flutter', 'Dart', 'Bloc', 'RevenueCat', 'Billplz'],
  },
  {
    icon: '🌐',
    name: 'Web Frontend',
    skills: ['Vue.js', 'JavaScript', 'Tailwind CSS', 'HTML / CSS'],
  },
  {
    icon: '⚙️',
    name: 'Backend',
    skills: ['Firebase', 'Express.js', 'Laravel', '.NET / C#'],
  },
  {
    icon: '🗄️',
    name: 'Database',
    skills: ['Firestore', 'SQLite', 'MongoDB'],
  },
  {
    icon: '🛠️',
    name: 'Tools & DevOps',
    skills: ['Git', 'GitHub', 'DigitalOcean', 'Vercel', 'App Store', 'Google Play'],
  },
  {
    icon: '🤖',
    name: 'AI Tools',
    skills: ['Claude Code', 'GitHub Copilot'],
  },
]
</script>

<template>
  <section id="skills" class="section">
    <div class="container">
      <div class="section-eyebrow">Skills</div>
      <h2 class="section-title">What I Work With</h2>

      <div class="grid">
        <div v-for="cat in categories" :key="cat.name" class="card">
          <div class="icon">{{ cat.icon }}</div>
          <h3 class="cat-name">{{ cat.name }}</h3>
          <div class="skill-list">
            <span v-for="s in cat.skills" :key="s" class="skill">{{ s }}</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
}

.card {
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: 16px;
  padding: 24px;
  transition: all 0.25s;
}

.card:hover {
  border-color: rgba(124, 58, 237, 0.4);
  transform: translateY(-4px);
  box-shadow: 0 12px 36px rgba(0, 0, 0, 0.35);
}

.icon {
  font-size: 26px;
  margin-bottom: 12px;
}

.cat-name {
  font-size: 15px;
  font-weight: 600;
  color: var(--text-h);
  margin-bottom: 16px;
}

.skill-list {
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
}

.skill {
  font-size: 12px;
  font-weight: 500;
  padding: 4px 10px;
  border-radius: 6px;
  background: rgba(255, 255, 255, 0.04);
  border: 1px solid var(--border);
  color: var(--text);
}

@media (max-width: 768px) {
  .grid { grid-template-columns: repeat(2, 1fr); }
}

@media (max-width: 480px) {
  .grid { grid-template-columns: 1fr; }
}
</style>
