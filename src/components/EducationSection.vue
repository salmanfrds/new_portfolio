<script setup>
const certs = [
  {
    name: 'JavaScript Algorithms and Data Structures',
    org: 'freeCodeCamp',
  },
  {
    name: 'Foundational C# Certification',
    org: 'Microsoft & freeCodeCamp',
  },
  {
    name: 'Introduction to Computer Networking',
    org: 'Cisco Networking Academy',
  },
]
</script>

<template>
  <section id="education" class="section">
    <div class="container">
      <div class="section-eyebrow">Education & Certifications</div>
      <h2 class="section-title">Academic Background</h2>

      <div class="grid">
        <div class="edu-card">
          <div class="top-bar"></div>
          <div class="grad-icon">🎓</div>
          <p class="period">March 2023 – Present</p>
          <h3 class="degree">Bachelor of Information Technology</h3>
          <p class="school">International Islamic University Malaysia (IIUM)</p>
          <p class="location">Kuala Lumpur, Malaysia</p>
          <div class="highlights">
            <div class="hl">
              <span class="hl-num">3.78</span>
              <span class="hl-label">CGPA</span>
            </div>
            <div class="hl">
              <span class="hl-num">6×</span>
              <span class="hl-label">Dean's List</span>
            </div>
          </div>
          <span class="scholarship-badge">🏆 Azman Hashim Scholar</span>
        </div>

        <div class="certs-panel">
          <h3 class="certs-heading">Certifications</h3>
          <div class="cert-list">
            <div v-for="c in certs" :key="c.name" class="cert-item">
              <div class="cert-mark">✓</div>
              <div>
                <p class="cert-name">{{ c.name }}</p>
                <p class="cert-org">{{ c.org }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 24px;
  align-items: start;
}

.edu-card {
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: 16px;
  padding: 28px;
  position: relative;
  overflow: hidden;
}

.top-bar {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 3px;
  background: linear-gradient(to right, var(--accent), var(--accent-light));
}

.grad-icon {
  font-size: 30px;
  margin-bottom: 16px;
}

.period {
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--accent-light);
  margin-bottom: 10px;
}

.degree {
  font-size: 18px;
  font-weight: 700;
  color: var(--text-h);
  margin-bottom: 8px;
}

.school {
  font-size: 14px;
  color: var(--text);
  margin-bottom: 4px;
}

.location {
  font-size: 13px;
  color: var(--text-muted);
  margin-bottom: 24px;
}

.highlights {
  display: flex;
  gap: 28px;
  margin-bottom: 22px;
}

.hl {
  display: flex;
  flex-direction: column;
  gap: 2px;
}

.hl-num {
  font-size: 30px;
  font-weight: 800;
  color: var(--accent-light);
  letter-spacing: -0.5px;
  line-height: 1;
}

.hl-label {
  font-size: 12px;
  color: var(--text-muted);
}

.scholarship-badge {
  display: inline-flex;
  font-size: 13px;
  font-weight: 600;
  padding: 5px 14px;
  border-radius: 100px;
  background: rgba(124, 58, 237, 0.12);
  color: var(--accent-light);
  border: 1px solid rgba(124, 58, 237, 0.28);
}

.certs-panel {
  display: flex;
  flex-direction: column;
}

.certs-heading {
  font-size: 18px;
  font-weight: 700;
  color: var(--text-h);
  margin-bottom: 18px;
}

.cert-list {
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.cert-item {
  display: flex;
  align-items: flex-start;
  gap: 14px;
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: 12px;
  padding: 18px 20px;
  transition: border-color 0.2s, transform 0.2s;
}

.cert-item:hover {
  border-color: rgba(124, 58, 237, 0.4);
  transform: translateX(4px);
}

.cert-mark {
  width: 28px;
  height: 28px;
  border-radius: 50%;
  background: var(--accent-glow);
  border: 1px solid rgba(124, 58, 237, 0.3);
  color: var(--accent-light);
  font-size: 13px;
  font-weight: 700;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
  margin-top: 1px;
}

.cert-name {
  font-size: 14px;
  font-weight: 600;
  color: var(--text-h);
  margin-bottom: 4px;
}

.cert-org {
  font-size: 13px;
  color: var(--accent-light);
}

@media (max-width: 768px) {
  .grid { grid-template-columns: 1fr; }
}
</style>
