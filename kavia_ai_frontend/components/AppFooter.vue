<template>
  <footer class="footer-section">
    <div class="footer-top">
      <div class="footer-columns">
        <div class="footer-col footer-brand">
          <span class="footer-logo"></span>
          <div class="footer-company">
            <div class="company-name">KAVIA AI</div>
            <div class="company-desc">Kavia AI enables strategic management and rapid software delivery for teams—from preseed ideas to scale-ups and enterprise.</div>
            <div class="footer-socials">
              <a v-for="(icon, i) in socialIcons" :key="i" :href="icon.link" target="_blank" class="footer-social-link" :title="icon.name">
                <component :is="icon.icon"/>
              </a>
            </div>
          </div>
        </div>
        <div class="footer-col">
          <div class="footer-list-title">Product</div>
          <ul>
            <li><a href="#">Features</a></li>
            <li><a href="#">Integrations</a></li>
            <li><a href="#">Security</a></li>
            <li><a href="#">Product Updates</a></li>
          </ul>
        </div>
        <div class="footer-col">
          <div class="footer-list-title">Company</div>
          <ul>
            <li><a href="#">About Us</a></li>
            <li><a href="#">Careers</a></li>
            <li><a href="#">Contact</a></li>
            <li><a href="#">Press</a></li>
          </ul>
        </div>
        <div class="footer-col">
          <div class="footer-list-title">Developers</div>
          <ul>
            <li><a href="#">Docs</a></li>
            <li><a href="#">Status</a></li>
            <li><a href="#">API</a></li>
            <li><a href="#">Blog</a></li>
          </ul>
        </div>
      </div>
    </div>
    <div class="footer-bottom">
      <span class="copyright">© 2024 Kavia AI. All Rights Reserved.</span>
      <span class="footer-madeby">
        Made by <span style="color: #F26522; font-weight:600;">Kavia Team</span>
      </span>
    </div>
  </footer>
</template>

<script setup lang="ts">
const socialIcons = [
  { name: "LinkedIn", link: "#", icon: { template: `<svg width="22" height="22"><rect fill="#fff" width="22" height="22" rx="6"/><rect x="4" y="10" width="2" height="6" fill="#F26522"/><circle cx="5" cy="7" r="1" fill="#F26522"/><rect x="8" y="10" width="2" height="6" fill="#F26522"/><rect x="11" y="8" width="2" height="8" fill="#F26522"/></svg>` } },
  { name: "Twitter", link: "#", icon: { template: `<svg width="22" height="22"><circle fill="#fff" cx="11" cy="11" r="11"/><path d="M6 13c6 0 8-5 8-8v-.5c.6-.4 1.4-1 2-1.5-.5.2-1 .4-1.5.5.5-.3.9-.8 1.1-1.3-.5.3-1 .5-1.5.6C13 2.5 12.4 2 11.7 2c-1.3 0-2.3 1-2.3 2.3 0 .2 0 .3.1.4C7 4.5 6 4 5 3.2c-.3.6-.5 1.3-.5 2 .6-.4 1.3-.7 2-.8-.5.4-.9 1-.9 1.8 0 .4.1.7.2 1.1-1.6-.5-3.1-1.6-4-3 0 .2 0 .3 0 .5C2 6 2 7 2.7 7.6c-.5 0-.9-.2-1.2-.4v.1c0 1.6 1.1 2.8 2.7 3.1-.3.1-.6.1-.8.1-.2 0-.4 0-.6-.1.4 1.3 1.7 2.2 3.2 2.2z" fill="#F26522"/></svg>` } },
  { name: "Discord", link: "#", icon: { template: `<svg width="22" height="22"><rect fill="#fff" width="22" height="22" rx="6"/><ellipse cx="11" cy="12" rx="7" ry="6" fill="#F26522"/><circle cx="9" cy="13" r="1.1" fill="#fff"/><circle cx="13" cy="13" r="1.1" fill="#fff"/></svg>` } },
  { name: "GitHub", link: "#", icon: { template: `<svg width="22" height="22"><rect fill="#fff" width="22" height="22" rx="6"/><circle cx="11" cy="11" r="7" fill="#18151C"/><path d="M13 18v-2.6c0-.4-.1-.7-.3-1-1.3.3-2.6.3-4 .3a10.8 10.8 0 01-2-.1c.2-.3.3-.6.3-1 0-.8-.4-1.5-1.1-2 .5 0 1.4.5 2.6.5s2.2-.5 2.7-.5c-.1-.7-.4-1.2-.8-1.7-2.3 0-4-1.5-4-3.1 0-.6.2-1.2.6-1.7a4.6 4.6 0 014 2c.7-.1 1.6-.5 2.5-1-1.2-.6-2.3-2-2.3-3.3 0-.7.3-1.5.9-2 1.5 0 2.6 1.3 3 2.4a9.3 9.3 0 013.5 1c.3 0 .7.4.8.7.3.2.5.5.8.9z" fill="#F26522"/></svg>` } }
]
</script>

<style scoped>
.footer-section {
  background: linear-gradient(180deg, #221C1C 86%, #18151C 100%);
  color: #fff;
  width: 100vw;
  padding-top: 42px;
  margin-top: 32px;
}
.footer-top {
  width: 100%;
  max-width: 1300px;
  margin: 0 auto;
  padding: 0 40px 48px 40px;
}
.footer-columns {
  display: flex;
  gap: 42px;
  align-items: flex-start;
  justify-content: space-between;
  flex-wrap: wrap;
}
.footer-col {
  flex: 1 1 0;
  min-width: 180px;
  margin-right: 0;
  margin-bottom: 12px;
}
.footer-brand { min-width: 230px;}
.footer-logo {
  width: 38px;
  height: 38px;
  display: block;
  background: linear-gradient(135deg, #F26522 0%, #fa822a 100%);
  border-radius: 50%;
  margin-bottom: 10px;
  box-shadow: 0 2px 12px #F2652244;
}
.company-name {
  font-size: 1.1rem;
  font-weight: 700;
  margin-top: 2px;
  margin-bottom: 2px;
  letter-spacing: 1.2px;
}
.company-desc {
  font-size: 1rem;
  color: #b3b3b3;
  margin-bottom: 12px;
  font-weight: 400;
}
.footer-list-title {
  color: #fff;
  font-weight: 900;
  font-size: 1.03rem;
  margin-bottom: 9px;
  letter-spacing: 0.2px;
}
.footer-col ul {
  list-style: none;
  padding-left: 0;
  margin: 0;
}
.footer-col ul li {
  margin-bottom: 8px;
}
.footer-col ul li a {
  color: #b3b3b3;
  font-size: 1rem;
  text-decoration: none;
  transition: color 0.2s;
  font-weight: 500;
}
.footer-col ul li a:hover {
  color: #F26522;
  text-decoration: underline;
}
.footer-socials {
  display: flex;
  gap: 10px;
  margin-top: 12px;
  align-items: center;
}
.footer-social-link {
  display: inline-block;
  vertical-align: middle;
  width: 32px;
  height: 32px;
  border-radius: 50%;
  background: none;
  text-align: center;
  transition: transform 0.1s;
}
.footer-social-link:hover { transform: scale(1.07);}
.footer-social-link svg * {
  fill: #fff !important;
}
.footer-social-link:hover svg * {
  fill: #F26522 !important;
}

.footer-bottom {
  width: 100%;
  max-width: 1300px;
  margin: 0 auto;
  padding: 18px 40px 0 40px;
  font-size: 0.98rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: #b3b3b3;
  border-top: 1.2px solid #302827;
}
.footer-madeby {
  font-size: 0.98rem;
}
@media (max-width: 900px) {
  .footer-top, .footer-bottom { padding: 0 18px 36px 18px; }
  .footer-columns { gap: 10px; }
}
@media (max-width: 700px) {
  .footer-columns { flex-direction: column; gap: 14px;}
  .footer-col { min-width: 110px;}
  .footer-brand { min-width: 160px;}
  .footer-bottom { flex-direction: column; gap: 2px; text-align: center;}
}
</style>
