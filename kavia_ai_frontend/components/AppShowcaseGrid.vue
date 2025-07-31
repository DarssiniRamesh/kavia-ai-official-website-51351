<template>
  <section class="showcase-section">
    <h2 class="showcase-title">
      Built for Enterprise,
      <br>
      Simplified for Software Creators
    </h2>
    <div class="showcase-grid">
      <div v-for="(card, i) in showcaseCards" :key="i" class="showcase-card">
        <div class="showcase-image" :style="{backgroundColor: card.bg}">
          <!-- Replace below with actual product screenshots if available -->
          <svg v-if="card.icon" :width="64" :height="56"><use :xlink:href="card.icon" /></svg>
        </div>
        <div class="showcase-card-body">
          <div class="showcase-card-title">{{ card.title }}</div>
          <div class="showcase-card-desc">{{ card.desc }}</div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const showcaseCards = [
  {
    title: 'Lightning Fast App Creation',
    desc: 'Turn prompts into real, running projects instantly.',
    icon: '',
    bg: '#231D1D'
  },
  {
    title: 'Scalable Cloud Deployments',
    desc: 'From idea to production with secure hosting.',
    icon: '',
    bg: '#221C1C'
  },
  {
    title: 'Real-Time Collaboration',
    desc: 'Work with your team or AI in the same interface.',
    icon: '',
    bg: '#231D1D'
  },
  {
    title: 'AI-Powered Code Reviews',
    desc: 'Enterprise-grade reviews by Kavia AI on demand.',
    icon: '',
    bg: '#231D1D'
  },
  {
    title: 'Instant Integration',
    desc: 'Plug into third-party APIs, auth, and more—no sweat.',
    icon: '',
    bg: '#221C1C'
  },
  {
    title: 'Marketplace Ecosystem',
    desc: 'Explore, share, or buy extensions and plugins.',
    icon: '',
    bg: '#231D1D'
  }
]
</script>

<style scoped>
.showcase-section {
  margin: 36px auto 60px auto;
}
.showcase-title {
  text-align: center;
  font-size: 2.02rem;
  font-weight: 900;
  color: #fff;
  margin-bottom: 38px;
  line-height: 1.18;
  letter-spacing: 0.2px;
}
.showcase-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 32px;
  max-width: 1200px;
  margin: 0 auto;
}
.showcase-card {
  background: #221C1C;
  border-radius: 18px;
  box-shadow: 0 2px 24px #0004;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  min-height: 280px;
  transition: box-shadow 0.15s, transform 0.15s;
  border: 1.5px solid #282122;
}
.showcase-card:hover {
  box-shadow: 0 8px 36px #F2652222;
  transform: translateY(-4px) scale(1.012);
}
.showcase-image {
  min-height: 116px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: #231D1D;
  padding-top: 16px;
}
.showcase-card-body {
  flex: 1 0 auto;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  padding: 24px;
  justify-content: flex-start;
}
.showcase-card-title {
  font-size: 1.16rem;
  color: #fff;
  font-weight: 700;
  margin-bottom: 8px;
  text-align: left;
}
.showcase-card-desc {
  color: #b3b3b3;
  font-size: 1rem;
  font-weight: 400;
  line-height: 1.4;
  text-align: left;
}
@media (max-width: 900px) {
  .showcase-grid {
    grid-template-columns: 1fr;
    gap: 22px;
    max-width: 96vw;
  }
  .showcase-title { font-size: 1.1rem; }
  .showcase-card { min-height: 208px; }
}
</style>
