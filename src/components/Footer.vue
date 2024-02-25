<template>
  <footer>
    <div class="footer-content">
      <img src="@/assets/logo.svg" alt="Your App Logo" class="logo" />
      <p>&copy; Lou Bonafé</p>
    </div>
  </footer>
</template>

<style scoped>
footer {
  position: fixed;
  bottom: 0;
  left: 0;
  width: 100%;
  background: linear-gradient(to bottom, rgba(62, 13, 13, 0.2), rgba(62, 13, 13, 0.8));
  padding: 10px;
  text-align: center;
}

.footer-content {
  max-width: 1200px;
  margin: 0 auto;
}

.logo {
  max-width: 20px;
  margin-bottom: 10px;
}
</style>
