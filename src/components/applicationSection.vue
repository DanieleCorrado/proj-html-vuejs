<script>

export default {
  name: 'aboutnetwork'
}
</script>

<template>
  <section id="application">

    <div class="app-logo">
      <img src="../assets/img/logo-5.png" alt="Logo LESS">
    </div>

    <div class="app-logo">
      <img src="../assets/img/logo-1.png" alt="Logo Woocommerce">
    </div>

    <div class="app-logo">
      <img src="../assets/img/logo-2.png" alt="Logo Woocommerce">
    </div>

    <div class="app-logo">
      <img src="../assets/img/logo-3.png" alt="Logo Woocommerce">
    </div>

    <div class="app-logo">
      <img src="../assets/img/logo-4.png" alt="Logo Woocommerce">
    </div>

    <div class="app-logo">
      <img src="../assets/img/logo-5.png" alt="Logo LESS">
    </div>

  </section>
</template>

<style lang="scss" scoped>
@use '../styles/general.scss' as *;
@use '../styles/partials/variables.scss' as *;

#application {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 90%;
  margin: 0 auto;

  // Regole logo
  .app-logo {
    padding: 60px 0;
    width: calc(100% / 6 - 20px);
    text-align: center;

    img {
      width: 80%;
    }
  }
}
</style>