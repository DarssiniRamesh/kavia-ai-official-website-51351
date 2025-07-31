<template>
  <section class="intro-section">
    <div class="intro-card">
      <h2 class="intro-title">
        <span class="intro-highlight">Reimagining</span>
        <span>&nbsp;Software Product Development</span>
      </h2>
      <div class="intro-marquee">
        <span class="marquee-text">
          <span class="marquee-orange">From weekend ideas!</span>
          <span> From </span>
          <span class="marquee-bold">weekend</span>
          <span> ideas!</span>
        </span>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
// Presentational only
</script>

<style scoped>
.intro-section {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 320px;
  background: transparent;
  margin-top: 32px;
  margin-bottom: 48px;
}
.intro-card {
  position: relative;
  width: 100%;
  max-width: 900px;
  margin: 0 auto;
  background: rgba(28, 20, 31, 0.76);
  border-radius: 28px;
  box-shadow: 0 2px 32px #0000001a;
  padding: 54px 44px 40px 44px;
  display: flex;
  flex-direction: column;
  align-items: center;
  backdrop-filter: blur(2px);
  border: 1.5px solid #F2652222;
}
.intro-title {
  font-size: 2.1rem;
  font-weight: 800;
  margin-bottom: 32px;
  text-align: center;
  letter-spacing: 0.4px;
}
.intro-highlight {
  color: #F26522;
  background: linear-gradient(90deg, #F26522 40%, #fa822a 100%);
  font-weight: 900;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
.marquee-text {
  font-size: 1.45rem;
  font-weight: 700;
  color: #fff;
  display: inline-block;
  white-space: nowrap;
  text-shadow: 0 2px 8px #0004;
  letter-spacing: 0.1px;
  animation: move-left 8s linear infinite;
}
@keyframes move-left {
  0% { transform: translateX(0);}
  100% { transform: translateX(-180px);}
}
.marquee-orange {
  color: #F26522;
  font-weight: 800;
}
.marquee-bold {
  color: #F26522;
  font-weight: 900;
  font-style: italic;
}
@media (max-width: 900px) {
  .intro-card { padding: 28px 12px; border-radius: 18px;}
  .intro-title { font-size: 1.28rem; }
  .marquee-text { font-size: 1rem;}
}
</style>
