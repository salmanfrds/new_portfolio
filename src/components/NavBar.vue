<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const scrolled = ref(false)
const mobileOpen = ref(false)
const activeSection = ref('')

const links = [
  { id: 'experience', label: 'Experience' },
  { id: 'skills', label: 'Skills' },
  { id: 'projects', label: 'Projects' },
  { id: 'education', label: 'Education' },
]

function scrollTo(id) {
  document.getElementById(id)?.scrollIntoView({ behavior: 'smooth' })
  mobileOpen.value = false
}

function onScroll() {
  scrolled.value = window.scrollY > 40

  const scrollY = window.scrollY + 120
  const all = ['hero', ...links.map(l => l.id), 'contact']
  for (let i = all.length - 1; i >= 0; i--) {
    const el = document.getElementById(all[i])
    if (el && scrollY >= el.offsetTop) {
      activeSection.value = all[i]
      break
    }
  }
}

onMounted(() => window.addEventListener('scroll', onScroll, { passive: true }))
onUnmounted(() => window.removeEventListener('scroll', onScroll))
</script>

<template>
  <nav :class="{ scrolled }">
    <div class="nav-inner">
      <button class="logo" @click="scrollTo('hero')">SF</button>

      <div class="links" :class="{ open: mobileOpen }">
        <button
          v-for="link in links"
          :key="link.id"
          :class="{ active: activeSection === link.id }"
          @click="scrollTo(link.id)"
        >
          {{ link.label }}
        </button>
        <button class="cta" @click="scrollTo('contact')">Contact</button>
      </div>

      <button class="toggle" @click="mobileOpen = !mobileOpen" aria-label="Toggle menu">
        <span :style="mobileOpen ? 'transform: rotate(45deg) translate(5px,5px)' : ''"></span>
        <span :style="mobileOpen ? 'opacity:0' : ''"></span>
        <span :style="mobileOpen ? 'transform: rotate(-45deg) translate(5px,-5px)' : ''"></span>
      </button>
    </div>
  </nav>
</template>

<style scoped>
nav {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1000;
  padding: 20px 24px;
  transition: all 0.3s;
  border-bottom: 1px solid transparent;
}

nav.scrolled {
  padding: 14px 24px;
  background: var(--bg-nav);
  backdrop-filter: blur(16px);
  -webkit-backdrop-filter: blur(16px);
  border-bottom-color: var(--border);
}

.nav-inner {
  max-width: 920px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.logo {
  background: linear-gradient(135deg, var(--accent-light), #c4b5fd);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  border: none;
  font-size: 22px;
  font-weight: 800;
  letter-spacing: -0.5px;
  padding: 0;
}

.links {
  display: flex;
  align-items: center;
  gap: 2px;
}

.links button {
  background: none;
  border: none;
  color: var(--text);
  font-size: 14px;
  font-weight: 500;
  padding: 8px 14px;
  border-radius: 8px;
  transition: all 0.2s;
}

.links button:hover,
.links button.active {
  color: var(--text-h);
  background: rgba(255, 255, 255, 0.05);
}

.links button.active {
  color: var(--accent-light);
}

.cta {
  background: var(--accent) !important;
  color: #fff !important;
  font-weight: 600 !important;
  padding: 8px 18px !important;
  margin-left: 8px;
  transition: all 0.2s !important;
}

.cta:hover {
  background: #6d28d9 !important;
  transform: translateY(-1px);
}

.toggle {
  display: none;
  flex-direction: column;
  gap: 5px;
  background: none;
  border: none;
  padding: 4px;
}

.toggle span {
  display: block;
  width: 22px;
  height: 2px;
  background: var(--text-h);
  border-radius: 2px;
  transition: all 0.3s;
}

@media (max-width: 600px) {
  .toggle { display: flex; }

  .links {
    display: none;
    position: fixed;
    inset: 0;
    background: rgba(8, 12, 20, 0.97);
    flex-direction: column;
    justify-content: center;
    gap: 8px;
    z-index: -1;
  }

  .links.open { display: flex; }

  .links button {
    font-size: 20px;
    padding: 14px 32px;
    border-radius: 10px;
  }

  .cta { margin-left: 0 !important; }
}
</style>
