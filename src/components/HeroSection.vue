<script setup>
function scrollTo(id) {
  document.getElementById(id)?.scrollIntoView({ behavior: 'smooth' })
}
</script>

<template>
  <section id="hero" class="hero">
    <div class="orb orb-1"></div>
    <div class="orb orb-2"></div>

    <div class="hero-content">
      <div class="badge">
        <span class="dot"></span>
        Available for opportunities
      </div>

      <p class="greeting">Hello, I'm</p>
      <h1 class="name">Muhammad Salman<br />Firdaus</h1>
      <p class="role">Mobile App Developer & Full-Stack Engineer</p>
      <p class="desc">
        Final-year IT student (3.78 CGPA) at IIUM with 1+ year shipping production Flutter
        apps to App Store and Google Play. Building full-stack systems with Firebase, Vue.js,
        and Laravel in real company environments.
      </p>

      <div class="cta-row">
        <button class="btn-primary" @click="scrollTo('projects')">
          View Projects
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><line x1="5" y1="12" x2="19" y2="12"/><polyline points="12 5 19 12 12 19"/></svg>
        </button>
        <a href="mailto:salmanfird4@gmail.com" class="btn-outline">Get in Touch</a>
      </div>

      <div class="socials">
        <a href="https://github.com/salmanfrds" target="_blank" rel="noopener" aria-label="GitHub">
          <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
            <path d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.942.359.31.678.921.678 1.856 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z"/>
          </svg>
        </a>
        <a href="https://linkedin.com/in/salman-firdaus" target="_blank" rel="noopener" aria-label="LinkedIn">
          <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
            <path d="M19 3a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h14m-.5 15.5v-5.3a3.26 3.26 0 0 0-3.26-3.26c-.85 0-1.84.52-2.32 1.3v-1.11h-2.79v8.37h2.79v-4.93c0-.77.62-1.4 1.39-1.4a1.4 1.4 0 0 1 1.4 1.4v4.93h2.79M6.88 8.56a1.68 1.68 0 0 0 1.68-1.68c0-.93-.75-1.69-1.68-1.69a1.69 1.69 0 0 0-1.69 1.69c0 .93.76 1.68 1.69 1.68m1.39 9.94v-8.37H5.5v8.37h2.77z"/>
          </svg>
        </a>
        <a href="mailto:salmanfird4@gmail.com" aria-label="Email">
          <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/>
          </svg>
        </a>
      </div>

      <div class="stats">
        <div class="stat">
          <span class="stat-num">3.78</span>
          <span class="stat-label">CGPA</span>
        </div>
        <div class="divider"></div>
        <div class="stat">
          <span class="stat-num">1+</span>
          <span class="stat-label">Years in Industry</span>
        </div>
        <div class="divider"></div>
        <div class="stat">
          <span class="stat-num">1K+</span>
          <span class="stat-label">App Downloads</span>
        </div>
        <div class="divider"></div>
        <div class="stat">
          <span class="stat-num">6×</span>
          <span class="stat-label">Dean's List</span>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero {
  min-height: 100vh;
  display: flex;
  align-items: center;
  position: relative;
  overflow: hidden;
  padding: 120px 24px 80px;
}

.orb {
  position: absolute;
  border-radius: 50%;
  pointer-events: none;
  filter: blur(90px);
}

.orb-1 {
  width: 600px;
  height: 600px;
  background: radial-gradient(circle, rgba(124, 58, 237, 0.22) 0%, transparent 70%);
  top: -150px;
  left: -150px;
}

.orb-2 {
  width: 400px;
  height: 400px;
  background: radial-gradient(circle, rgba(79, 70, 229, 0.15) 0%, transparent 70%);
  bottom: 0;
  right: -100px;
}

.hero-content {
  max-width: 920px;
  margin: 0 auto;
  width: 100%;
  position: relative;
  z-index: 1;
}

.badge {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  background: rgba(16, 185, 129, 0.1);
  border: 1px solid rgba(16, 185, 129, 0.25);
  color: #34d399;
  font-size: 13px;
  font-weight: 500;
  padding: 6px 14px;
  border-radius: 100px;
  margin-bottom: 28px;
}

.dot {
  width: 7px;
  height: 7px;
  border-radius: 50%;
  background: #10b981;
  animation: pulse 2s ease-in-out infinite;
}

@keyframes pulse {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.35; }
}

.greeting {
  font-size: 18px;
  color: var(--accent-light);
  font-weight: 500;
  margin-bottom: 6px;
}

.name {
  font-size: 68px;
  font-weight: 800;
  letter-spacing: -2.5px;
  line-height: 1.04;
  margin-bottom: 20px;
  background: linear-gradient(135deg, #e2e8f0 30%, #a78bfa 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.role {
  font-size: 20px;
  color: var(--accent-light);
  font-weight: 500;
  margin-bottom: 20px;
}

.desc {
  font-size: 17px;
  color: var(--text);
  max-width: 580px;
  line-height: 1.75;
  margin-bottom: 36px;
}

.cta-row {
  display: flex;
  gap: 12px;
  align-items: center;
  margin-bottom: 32px;
  flex-wrap: wrap;
}

.btn-primary {
  background: var(--accent);
  border: none;
  color: #fff;
  font-size: 15px;
  font-weight: 600;
  padding: 12px 24px;
  border-radius: 10px;
  display: flex;
  align-items: center;
  gap: 8px;
  transition: all 0.2s;
}

.btn-primary:hover {
  background: #6d28d9;
  transform: translateY(-2px);
  box-shadow: 0 10px 28px rgba(124, 58, 237, 0.4);
}

.btn-outline {
  color: var(--text-h);
  font-size: 15px;
  font-weight: 600;
  padding: 12px 24px;
  border-radius: 10px;
  border: 1px solid var(--border);
  transition: all 0.2s;
  display: inline-block;
}

.btn-outline:hover {
  border-color: var(--accent-light);
  color: var(--accent-light);
  background: var(--accent-glow);
}

.socials {
  display: flex;
  gap: 10px;
  margin-bottom: 52px;
}

.socials a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 42px;
  height: 42px;
  border-radius: 10px;
  background: var(--bg-card);
  border: 1px solid var(--border);
  color: var(--text);
  transition: all 0.2s;
}

.socials a:hover {
  color: var(--accent-light);
  border-color: rgba(167, 139, 250, 0.5);
  background: var(--accent-glow);
  transform: translateY(-2px);
}

.stats {
  display: flex;
  align-items: center;
  gap: 28px;
  flex-wrap: wrap;
}

.stat {
  display: flex;
  flex-direction: column;
  gap: 2px;
}

.stat-num {
  font-size: 28px;
  font-weight: 800;
  color: var(--text-h);
  letter-spacing: -0.5px;
  line-height: 1;
}

.stat-label {
  font-size: 12px;
  color: var(--text-muted);
}

.divider {
  width: 1px;
  height: 36px;
  background: var(--border);
}

@media (max-width: 768px) {
  .name {
    font-size: 42px;
    letter-spacing: -1.5px;
  }
  .role { font-size: 16px; }
  .desc { font-size: 15px; }
  .stats { gap: 20px; }
  .stat-num { font-size: 22px; }
}
</style>
