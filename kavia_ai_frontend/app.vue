<template>
  <div id="kavia-app" class="bg-canvas text-primary">
    <AppNavbar />
    <main class="main-content">
      <AppHeroHeader />
      <AppIntroCard />
      <AppShowcaseGrid />
    </main>
    <AppFooter />
  </div>
</template>

<script setup lang="ts">
import AppNavbar from '~/components/AppNavbar.vue'
import AppHeroHeader from '~/components/AppHeroHeader.vue'
import AppIntroCard from '~/components/AppIntroCard.vue'
import AppShowcaseGrid from '~/components/AppShowcaseGrid.vue'
import AppFooter from '~/components/AppFooter.vue'
</script>

<style>
body, #__nuxt, #kavia-app {
  min-height: 100vh;
  margin: 0;
  font-family: 'Helvetica Neue', Arial, sans-serif;
  background: var(--bg-canvas, #18151C);
  color: var(--text-primary, #fff);
}
#kavia-app {
  min-height: 100vh;
  width: 100vw;
  background: var(--bg-canvas);
  display: flex;
  flex-direction: column;
}
.main-content {
  flex: 1 0 auto;
  width: 100%;
  max-width: 1300px;
  margin: 0 auto;
  padding: 48px 0 0 0;
}
</style>
