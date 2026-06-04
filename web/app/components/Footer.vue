<template>
  <div class="footer-wrapper">
    <div class="content">
      <Button color="orange" @click="navigateTo('/spenden')">Jetzt Spenden</Button>
      <Button color="blue" outlined @click="navigateTo('/kontakt')">Kontakt</Button>
    </div>

    <div class="links">
      <FooterLink size="medium" @click="navigateTo('/impressum')">Impressum</FooterLink>
      <FooterLink size="medium" @click="navigateTo('/datenschutz')">Datenschutz</FooterLink>
      <p class="copyright">© 2026 SOS Wohnunglosenhilfe e.V.</p>
    </div>
  </div>
</template>

<script setup>
import FooterLink from './FooterLink.vue';
</script>

<style scoped>
.footer-wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  border-top: 5px solid var(--lightblue);
  padding-top: 40px;
  margin-top: 80px;
  padding-bottom: 36px;
  gap: 16px;
}

.content {
  display: flex;
  gap: 36px;
  margin-top: 10px;
}

.links {
  display: flex;
  flex-direction: column;
  gap: 10px;
  align-items: center;
  text-align: center;
  margin-top: 15px;
}

.copyright {
  font-size: 18px;
  font-weight: 200;
  color: var(--gray);
  margin-top: 5px;
}

@media (min-width: 1024px) {
  .links {
    flex-direction: row;
    gap: 20px;
    flex-wrap: wrap;
    justify-content: center;
    margin-top: 0;
  }

  .footer-wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    border-top: 5px solid var(--lightblue);
    padding-top: 40px;
    padding-bottom: 36px;
    gap: 36px;
  }

  .copyright {
    margin-top: 0;
  }
}
</style>