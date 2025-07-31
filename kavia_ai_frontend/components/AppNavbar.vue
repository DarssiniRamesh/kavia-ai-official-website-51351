<template>
  <nav class="kavia-navbar">
    <div class="navbar-inner">
      <div class="navbar-left flex items-center gap-3">
        <img src="@/assets/kavia_logo.png" alt="Kavia AI Logo" class="kavia-logo-img" />
        <span class="kavia-logo-text">KAVIA AI</span>
      </div>
      <ul class="navbar-center">
        <li><a href="#">Product</a></li>
        <li><a href="#">Solutions</a></li>
        <li><a href="#">Community</a></li>
        <li><a href="#">Pricing</a></li>
        <li><a href="#">Developers</a></li>
      </ul>
      <div class="navbar-right flex items-center gap-2">
        <a class="contact-link" href="#">Contact</a>
        <a class="signin-btn" href="#">SIGN IN</a>
      </div>
    </div>
  </nav>
</template>

<script setup lang="ts">
// No logic required - purely presentational
</script>

<style scoped>
.kavia-navbar {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 56px;
  background: #18151C;
  box-shadow: 0 1px 12px 0 rgba(0,0,0,0.08);
  z-index: 1000;
  display: flex;
  align-items: center;
}
.navbar-inner {
  width: 100%;
  max-width: 1300px;
  margin: 0 auto;
  height: 56px;
  padding: 0 48px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.kavia-logo-img {
  width: 28px;
  height: 28px;
  border-radius: 50%;
  margin-right: 8px;
  object-fit: cover;
  background: #fff;
  box-shadow: 0 1px 8px #f265220d;
}
.kavia-logo-text {
  font-weight: 800;
  color: #fff;
  font-size: 1.25rem;
  letter-spacing: 1.5px;
  font-family: "Helvetica Neue", Arial, sans-serif;
  line-height: 1;
}
.navbar-center {
  flex: 1 1 0%;
  display: flex;
  gap: 32px;
  justify-content: center;
  align-items: center;
  list-style: none;
  margin: 0;
  padding: 0;
}
.navbar-center li a {
  color: #fff;
  font-size: 1rem;
  font-weight: 700;
  letter-spacing: 0.5px;
  text-transform: uppercase;
  padding: 4px 0;
  text-decoration: none;
  transition: color 0.2s;
}
.navbar-center li a:hover {
  color: #F26522;
}
.navbar-right .contact-link {
  color: #fff;
  text-decoration: none;
  font-size: 1rem;
  font-weight: 600;
  margin-right: 10px;
  transition: color 0.2s;
}
.navbar-right .contact-link:hover {
  color: #F26522;
}
.navbar-right .signin-btn {
  display: inline-block;
  background: #F26522;
  color: #fff;
  font-weight: 700;
  padding: 8px 22px;
  border-radius: 22px;
  letter-spacing: 1px;
  text-transform: uppercase;
  text-decoration: none;
  box-shadow: 0 1px 6px 0 #f2652230;
  transition: background 0.2s, box-shadow 0.2s;
}
.navbar-right .signin-btn:hover {
  background: #FA822A;
  box-shadow: 0 2px 16px 0 #f2652240;
}
@media (max-width: 900px) {
  .navbar-inner {
    padding: 0 16px;
  }
  .navbar-center {
    gap: 20px;
  }
}
@media (max-width: 768px) {
  .navbar-inner {
    padding: 0 8px;
  }
  .navbar-center {
    display: none; /* hamburger/mobile menu needed, outside this scope */
  }
}
</style>
