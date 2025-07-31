<template>
  <section class="hero-section">
    <div class="hero-inner">
      <span class="sparkle-star" aria-hidden="true">★</span>
      <h1 class="hero-title">What do you want to build today?</h1>
      <div class="hero-input-row">
        <input class="hero-input" type="text" placeholder="How can KAVIA help you today?" />
        <span class="send-icon" aria-label="Send">
          <svg width="26" height="26" viewBox="0 0 24 24" fill="none">
            <path d="M4 20L20 12L4 4V10L16 12L4 14V20Z"
                  fill="#b2afbb"/>
          </svg>
        </span>
      </div>
      <div class="hero-btn-group">
        <button class="hero-pill-btn selected">Web</button>
        <button class="hero-pill-btn">Mobile</button>
        <button class="hero-pill-btn">Backend</button>
        <button class="hero-pill-btn">Fullstack</button>
      </div>
      <div class="hero-framework-row">
        <span v-for="fw in frameworks" :key="fw.name" class="framework-icon" :title="fw.name"
              :class="{ active: activeFramework === fw.name }"
              @mouseover="activeFramework = fw.name"
              @mouseleave="activeFramework = ''">
          <component :is="fw.icon" />
        </span>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref } from 'vue'
const activeFramework = ref('')
const frameworks = [
  { name: 'Vue', icon: { template: '<svg width="24" height="24"><circle cx="12" cy="12" r="9" fill="#b2afbb"/></svg>' } },
  { name: 'React', icon: { template: '<svg width="24" height="24"><rect width="18" height="18" x="3" y="3" rx="6" fill="#b2afbb"/></svg>' } },
  { name: 'Angular', icon: { template: '<svg width="24" height="24"><polygon points="12,3 21,21 3,21" fill="#b2afbb"/></svg>' } },
  { name: 'Nuxt', icon: { template: '<svg width="24" height="24"><path d="M12 4 L20 20 H4z" fill="#b2afbb" /></svg>' } },
  { name: 'Node', icon: { template: '<svg width="24" height="24"><ellipse cx="12" cy="12" rx="9" ry="7" fill="#b2afbb"/></svg>' } },
  { name: 'Next.js', icon: { template: '<svg width="24" height="24"><circle cx="12" cy="12" r="10" stroke="#b2afbb" stroke-width="2" fill="none"/></svg>' } },
  { name: 'Svelte', icon: { template: '<svg width="24" height="24"><rect width="20" height="10" x="2" y="7" rx="5" fill="#b2afbb"/></svg>' } },
  { name: 'Flutter', icon: { template: '<svg width="24" height="24"><polygon points="4,20 20,4 20,20" fill="#b2afbb"/></svg>' } },
  { name: 'FastAPI', icon: { template: '<svg width="24" height="24"><rect width="12" height="12" x="6" y="6" fill="#b2afbb"/></svg>' } },
  { name: 'Python', icon: { template: '<svg width="24" height="24"><circle cx="12" cy="12" r="7" fill="#b2afbb"/></svg>' } },
  // add more as needed...
]
</script>

<style scoped>
.hero-section {
  background: var(--bg-canvas, #17141a);
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 570px;
  padding-top: 90px;
  padding-bottom: 32px;
}
.hero-inner {
  width: 100%;
  max-width: 640px;
  margin: 0 auto;
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.sparkle-star {
  font-size: 2.8rem;
  color: #FF7C1E;
  display: block;
  margin-bottom: 16px;
  filter: drop-shadow(0 2px 8px #ff7c1e44);
}
.hero-title {
  font-size: 2.4rem;
  font-weight: 800;
  color: #fff;
  margin-bottom: 32px;
  letter-spacing: 0.25px;
  text-align: center;
  line-height: 1.1;
}
.hero-input-row {
  display: flex;
  align-items: center;
  background: #222025;
  border: 1px solid #474250;
  border-radius: 14px;
  width: 100%;
  max-width: 570px;
  height: 56px;
  position: relative;
  margin: 0 auto 22px auto;
}
.hero-input {
  flex: 1 1 auto;
  background: transparent;
  border: none;
  color: #fff;
  font-size: 1.12rem;
  padding: 0 20px;
  height: 56px;
  outline: none;
}
.hero-input::placeholder {
  color: #b2afbb;
  opacity: 0.8;
  font-weight: 400;
}
.send-icon {
  width: 38px;
  height: 38px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-right: 10px;
  cursor: pointer;
  transition: filter 0.15s;
}
.send-icon:hover svg path {
  fill: #FF7C1E;
}
.hero-btn-group {
  display: flex;
  gap: 10px;
  margin-bottom: 32px;
}
.hero-pill-btn {
  padding: 10px 24px;
  border: none;
  background: #222025;
  color: #b2afbb;
  border-radius: 24px;
  font-weight: 500;
  font-size: 1rem;
  cursor: pointer;
  letter-spacing: 0.5px;
  transition: background 0.15s, color 0.15s, box-shadow 0.2s;
  box-shadow: none;
  text-transform: capitalize;
}
.hero-pill-btn.selected,
.hero-pill-btn:hover {
  background: #FF7C1E;
  color: #fff;
  box-shadow: 0 2px 8px #ff7c1e22;
}
.hero-framework-row {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 16px;
  margin-top: 32px;
}
.framework-icon {
  width: 44px;
  height: 44px;
  border-radius: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  background: none;
  cursor: pointer;
  transition: background 0.1s, transform 0.1s;
  border: none;
  font-size: 1.15rem;
}
.framework-icon.active,
.framework-icon:hover {
  background: #232027;
  box-shadow: 0 2px 10px #ff7c1e30;
}
.framework-icon.active svg *, .framework-icon:hover svg * {
  fill: #FF7C1E !important;
  stroke: #FF7C1E !important;
}
@media (max-width: 700px) {
  .hero-inner {
    max-width: 95vw;
  }
  .hero-title { font-size: 2rem; }
  .hero-input-row { max-width: 95vw; }
}
@media (max-width: 480px) {
  .hero-section {
    padding-top: 60px;
    min-height: 400px;
  }
  .hero-inner { padding: 0; }
  .hero-title { font-size: 1.33rem; }
  .hero-framework-row { gap: 10px; }
  .hero-btn-group { flex-wrap: wrap; gap: 7px; }
}
</style>
