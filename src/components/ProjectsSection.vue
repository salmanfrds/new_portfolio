<script setup>
const projects = [
  {
    title: 'MicroOps',
    subtitle: 'Management System for Micro-Enterprises (FYP)',
    status: 'ongoing',
    desc: 'Full-stack business management platform for micro-enterprises with real-time data synchronization and a scalable NoSQL schema. Currently in beta testing.',
    tags: ['Vue.js', 'Firebase', 'Firestore', 'Real-time Sync'],
  },
  {
    title: 'QRoll',
    subtitle: 'QR-Based Attendance System',
    status: 'ongoing',
    desc: 'Cross-platform attendance system featuring QR code generation, token-based session validation, and secure authentication via Laravel Sanctum.',
    tags: ['Flutter', 'Dart', 'Laravel', 'Laravel Sanctum', 'QR Code'],
  },
  {
    title: 'Yayasan Anggur Sejahtera',
    subtitle: 'Official Foundation Website',
    status: 'archived',
    desc: 'Responsive web platform with a custom CRUD architecture for announcements, managing the full deployment lifecycle on DigitalOcean.',
    tags: ['Tailwind CSS', 'Express.js', 'DigitalOcean'],
  },
]
</script>

<template>
  <section id="projects" class="section projects-section">
    <div class="container">
      <div class="section-eyebrow">Projects</div>
      <h2 class="section-title">Things I've Built</h2>

      <div class="grid">
        <div v-for="p in projects" :key="p.title" class="card">
          <div class="card-top">
            <span class="status" :class="p.status">
              {{ p.status === 'ongoing' ? '● Ongoing' : '○ Archived' }}
            </span>
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="folder-icon"><path d="M22 19a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h5l2 3h9a2 2 0 0 1 2 2z"/></svg>
          </div>
          <h3 class="proj-title">{{ p.title }}</h3>
          <p class="proj-subtitle">{{ p.subtitle }}</p>
          <p class="proj-desc">{{ p.desc }}</p>
          <div class="tags">
            <span v-for="t in p.tags" :key="t" class="tag">{{ t }}</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.projects-section {
  background: var(--bg-secondary);
}

.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
  align-items: stretch;
}

.card {
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: 16px;
  padding: 26px;
  display: flex;
  flex-direction: column;
  transition: all 0.25s;
  position: relative;
  overflow: hidden;
}

.card::before {
  content: '';
  position: absolute;
  inset: 0;
  background: linear-gradient(135deg, var(--accent-glow) 0%, transparent 60%);
  opacity: 0;
  transition: opacity 0.25s;
  pointer-events: none;
}

.card:hover {
  border-color: rgba(124, 58, 237, 0.5);
  transform: translateY(-5px);
  box-shadow: 0 16px 48px rgba(0, 0, 0, 0.4);
}

.card:hover::before {
  opacity: 1;
}

.card-top {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 18px;
}

.status {
  font-size: 12px;
  font-weight: 600;
}

.status.ongoing {
  color: var(--accent-light);
}

.status.archived {
  color: var(--text-muted);
}

.folder-icon {
  color: var(--accent-light);
  opacity: 0.6;
}

.proj-title {
  font-size: 19px;
  font-weight: 700;
  color: var(--text-h);
  margin-bottom: 5px;
}

.proj-subtitle {
  font-size: 13px;
  color: var(--accent-light);
  font-weight: 500;
  margin-bottom: 14px;
}

.proj-desc {
  font-size: 14px;
  line-height: 1.7;
  color: var(--text);
  flex-grow: 1;
  margin-bottom: 22px;
}

.tags {
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
  margin-top: auto;
}

.tag {
  font-size: 11px;
  font-weight: 600;
  padding: 3px 9px;
  border-radius: 5px;
  background: rgba(255, 255, 255, 0.04);
  border: 1px solid var(--border);
  color: var(--text-muted);
}

@media (max-width: 768px) {
  .grid { grid-template-columns: 1fr; }
}
</style>
