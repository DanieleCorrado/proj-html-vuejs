<script>
import PageHeader from './components/PageHeader.vue';
import PageMain from './components/PageMain.vue';
import PageFooter from './components/PageFooter.vue';

export default {
  components: {
    PageHeader,
    PageMain,
    PageFooter
  }
}
</script>

<template>

  <header>
    <PageHeader/>
  </header>
  
  <main>
    <PageMain/>
  </main>
  
  <footer>
    <PageFooter/>
  </footer>


</template>

<style lang="scss" scoped>

@use './styles/general.scss' as *;


</style>
