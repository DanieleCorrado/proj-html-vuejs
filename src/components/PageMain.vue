<script>

import contacts from '../dataset/contacts.json';
import logisticSection from './logisticSection.vue';
import aboutnetwork from './aboutnetwork.vue';
import applicationSection from './applicationSection.vue';
import newsSection from './newsSection.vue';
import newsletterSection from './newsletterSection.vue';
import getInTouchSection from './getInTouchSection.vue';
import store from '../dataset/store.json';

export default {
  name: "PageMain",
  components: {
    logisticSection,
    aboutnetwork,
    applicationSection,
    newsSection,
    newsletterSection,
    getInTouchSection,
  }
}
</script>

<template>
  <main>

    <!-- Sezione loistica -->

    <logisticSection />

    <!-- Sezione about network -->

    <aboutnetwork />


    <!-- Sezione applicativi -->

    <applicationSection />


    <!-- Sezione news -->

    <newsSection />

    <!-- Sezione newsletter -->

    <newsletterSection />

    <!-- Sezione get in touch -->

    <getInTouchSection />

  </main>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;

main {
  background-color: $mainbackground;
}
</style>
