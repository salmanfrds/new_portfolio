<script setup>
const jobs = [
  {
    title: 'Mobile App Developer',
    company: 'DeTA Technologies',
    period: 'Dec 2025 – Present',
    location: 'Kuala Lumpur',
    bullets: [
      'Launched Aurum and Bucava MVPs achieving 1,000+ downloads on App Store and Google Play, bridging Flutter frontends with .NET/Firebase backends and RevenueCat.',
      'Developed robust Flutter frontends for the dual-app Spana ecosystem (Customer app live, Business app in progress) with seamless payment gateway integrations via Billplz.',
      'Managed version control using GitHub with pull requests and branch management within an Agile development environment.',
    ],
    tags: ['Flutter', 'Dart', 'Firebase', '.NET / C#', 'RevenueCat', 'Billplz'],
  },
  {
    title: 'Lead Web Development Core Team',
    company: 'Google Developer Group on Campus (GDGoC) IIUM',
    period: 'Nov 2024 – Present',
    location: 'Kuala Lumpur',
    bullets: [
      'Led mobile development training for 235+ students by architecting the curriculum and conducting comprehensive, hands-on Flutter and Firebase workshops.',
      'Engineered the Kitahack 2025 website with Tailwind CSS, supporting 400+ active participants.',
    ],
    tags: ['Flutter', 'Firebase', 'Tailwind CSS', 'Workshop Facilitation'],
  },
  {
    title: 'Web Developer',
    company: 'Persatuan Pelajar Indonesia IIUM',
    period: 'Jan 2025 – Dec 2025',
    location: 'Kuala Lumpur',
    bullets: [
      'Developed the official PPI-IIUM website and custom CMS (Vue.js, Express, MongoDB), centralizing organization resources for 2,000+ visitors and 7,000+ annual page views.',
    ],
    tags: ['Vue.js', 'Express.js', 'MongoDB'],
  },
]
</script>

<template>
  <section id="experience" class="section exp-section">
    <div class="container">
      <div class="section-eyebrow">Experience</div>
      <h2 class="section-title">Where I've Worked</h2>

      <div class="timeline">
        <div v-for="job in jobs" :key="job.company" class="timeline-item">
          <div class="dot"></div>
          <div class="card">
            <div class="card-top">
              <div>
                <h3 class="job-title">{{ job.title }}</h3>
                <p class="company">{{ job.company }}</p>
              </div>
              <div class="meta">
                <span>{{ job.period }}</span>
                <span>{{ job.location }}</span>
              </div>
            </div>
            <ul class="bullets">
              <li v-for="b in job.bullets" :key="b">{{ b }}</li>
            </ul>
            <div class="tags">
              <span v-for="t in job.tags" :key="t" class="tag">{{ t }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.exp-section {
  background: var(--bg-secondary);
}

.timeline {
  position: relative;
  padding-left: 32px;
}

.timeline::before {
  content: '';
  position: absolute;
  left: 5px;
  top: 16px;
  bottom: 24px;
  width: 2px;
  background: linear-gradient(to bottom, var(--accent) 0%, rgba(124, 58, 237, 0.1) 100%);
  border-radius: 1px;
}

.timeline-item {
  position: relative;
  margin-bottom: 24px;
}

.timeline-item:last-child {
  margin-bottom: 0;
}

.dot {
  position: absolute;
  left: -27px;
  top: 20px;
  width: 12px;
  height: 12px;
  border-radius: 50%;
  background: var(--accent);
  border: 2px solid var(--bg-secondary);
  box-shadow: 0 0 0 4px var(--accent-glow);
}

.card {
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: 16px;
  padding: 26px;
  transition: border-color 0.25s, transform 0.25s;
}

.card:hover {
  border-color: rgba(124, 58, 237, 0.45);
  transform: translateX(4px);
}

.card-top {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  gap: 16px;
  margin-bottom: 18px;
  flex-wrap: wrap;
}

.job-title {
  font-size: 17px;
  font-weight: 700;
  color: var(--text-h);
  margin-bottom: 5px;
}

.company {
  font-size: 14px;
  color: var(--accent-light);
  font-weight: 500;
}

.meta {
  text-align: right;
  flex-shrink: 0;
  display: flex;
  flex-direction: column;
  gap: 3px;
}

.meta span {
  font-size: 13px;
  color: var(--text-muted);
}

.bullets {
  margin-bottom: 18px;
}

.bullets li {
  position: relative;
  padding-left: 18px;
  font-size: 14px;
  line-height: 1.7;
  margin-bottom: 10px;
  color: var(--text);
}

.bullets li:last-child {
  margin-bottom: 0;
}

.bullets li::before {
  content: '▸';
  position: absolute;
  left: 0;
  color: var(--accent-light);
  font-size: 11px;
  top: 3px;
}

.tags {
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
}

.tag {
  font-size: 12px;
  font-weight: 500;
  padding: 3px 10px;
  border-radius: 100px;
  background: var(--accent-glow);
  color: var(--accent-light);
  border: 1px solid rgba(124, 58, 237, 0.2);
}

@media (max-width: 600px) {
  .card-top { flex-direction: column; }
  .meta { text-align: left; }
}
</style>
