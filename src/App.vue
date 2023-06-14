<!-- Bisogna cambiare prima di tutto le cose della composition API, dato che usiamo l'options API -->
<script>
import PageHeader from './components/PageHeader.vue';
import PageFooter from './components/PageFooter.vue';
import FoodCorner from './components/FoodCorner.vue';

export default {
  components: {
    PageHeader,
    PageFooter,
    FoodCorner
  }
}
</script>

<template>
  <!-- Il template si divide in sections -->
  <section>
    <PageHeader />
  </section>
  <section>
    <PageFooter />
  </section>
  <section>
    <FoodCorner />
  </section>
</template>

<style lang="scss">
@use './styles/partials/variables.scss' as *;
@use './styles/general.scss' as *;

body {
  background-color: $bianco;
}
</style>
