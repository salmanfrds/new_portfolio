<template>
  <section id="contact" class="contact">
    <div class="glow"></div>
    <div class="contact-inner">
      <p class="eyebrow">Get in Touch</p>
      <h2 class="title">Let's Work Together</h2>
      <p class="desc">
        I'm currently open to new opportunities — whether you have a project in mind,
        a job offer, or just want to say hi. My inbox is always open!
      </p>
      <a href="mailto:salmanfird4@gmail.com" class="cta-btn">
        Say Hello 👋
      </a>

      <div class="socials">
        <a href="https://github.com/salmanfrds" target="_blank" rel="noopener">
          <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor">
            <path d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.942.359.31.678.921.678 1.856 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z"/>
          </svg>
          GitHub
        </a>
        <a href="https://linkedin.com/in/salman-firdaus" target="_blank" rel="noopener">
          <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor">
            <path d="M19 3a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h14m-.5 15.5v-5.3a3.26 3.26 0 0 0-3.26-3.26c-.85 0-1.84.52-2.32 1.3v-1.11h-2.79v8.37h2.79v-4.93c0-.77.62-1.4 1.39-1.4a1.4 1.4 0 0 1 1.4 1.4v4.93h2.79M6.88 8.56a1.68 1.68 0 0 0 1.68-1.68c0-.93-.75-1.69-1.68-1.69a1.69 1.69 0 0 0-1.69 1.69c0 .93.76 1.68 1.69 1.68m1.39 9.94v-8.37H5.5v8.37h2.77z"/>
          </svg>
          LinkedIn
        </a>
        <a href="tel:+601116854708">
          <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07A19.5 19.5 0 0 1 4.69 12 19.79 19.79 0 0 1 1.61 3.42 2 2 0 0 1 3.6 1.27h3a2 2 0 0 1 2 1.72c.127.96.361 1.903.7 2.81a2 2 0 0 1-.45 2.11L7.91 8.91a16 16 0 0 0 6 6l.91-.91a2 2 0 0 1 2.11-.45c.907.339 1.85.573 2.81.7A2 2 0 0 1 21.73 16.92z"/>
          </svg>
          +601116854708
        </a>
      </div>
    </div>
  </section>

  <footer>
    <div class="footer-inner">
      <p class="footer-name">Muhammad Salman Firdaus</p>
      <p class="footer-copy">Built with Vue.js & Vite · Kuala Lumpur, Malaysia</p>
    </div>
  </footer>
</template>

<style scoped>
.contact {
  padding: 120px 24px;
  text-align: center;
  border-top: 1px solid var(--border);
  position: relative;
  overflow: hidden;
}

.glow {
  position: absolute;
  top: -200px;
  left: 50%;
  transform: translateX(-50%);
  width: 700px;
  height: 500px;
  background: radial-gradient(ellipse, rgba(124, 58, 237, 0.1) 0%, transparent 65%);
  pointer-events: none;
}

.contact-inner {
  position: relative;
  z-index: 1;
  max-width: 560px;
  margin: 0 auto;
}

.eyebrow {
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--accent-light);
  margin-bottom: 16px;
}

.title {
  font-size: 52px;
  font-weight: 800;
  letter-spacing: -1.5px;
  margin-bottom: 20px;
  background: linear-gradient(135deg, #e2e8f0 30%, #a78bfa 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.desc {
  font-size: 16px;
  line-height: 1.75;
  color: var(--text);
  margin-bottom: 36px;
}

.cta-btn {
  display: inline-block;
  background: var(--accent);
  color: #fff;
  font-size: 16px;
  font-weight: 600;
  padding: 14px 36px;
  border-radius: 12px;
  transition: all 0.2s;
  margin-bottom: 44px;
}

.cta-btn:hover {
  background: #6d28d9;
  color: #fff;
  transform: translateY(-2px);
  box-shadow: 0 14px 36px rgba(124, 58, 237, 0.4);
}

.socials {
  display: flex;
  justify-content: center;
  gap: 16px;
  flex-wrap: wrap;
}

.socials a {
  display: inline-flex;
  align-items: center;
  gap: 7px;
  font-size: 14px;
  font-weight: 500;
  color: var(--text-muted);
  padding: 8px 16px;
  border-radius: 8px;
  border: 1px solid var(--border);
  background: var(--bg-card);
  transition: all 0.2s;
}

.socials a:hover {
  color: var(--accent-light);
  border-color: rgba(167, 139, 250, 0.4);
  background: var(--accent-glow);
}

footer {
  background: var(--bg-secondary);
  border-top: 1px solid var(--border);
  padding: 24px;
}

.footer-inner {
  max-width: 920px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 8px;
}

.footer-name {
  font-size: 14px;
  font-weight: 600;
  color: var(--text-h);
}

.footer-copy {
  font-size: 13px;
  color: var(--text-muted);
}

@media (max-width: 600px) {
  .title { font-size: 36px; }
  .footer-inner { justify-content: center; text-align: center; }
}
</style>
