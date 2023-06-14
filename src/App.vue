<!-- Bisogna cambiare prima di tutto le cose della composition API, dato che usiamo l'options API -->
<script>
import PageHeader from './components/PageHeader.vue';
import PageFooter from './components/PageFooter.vue';
import FoodCorner from './components/FoodCorner.vue';
import PopularRecipes from './components/PopularRecipes.vue';

export default {
  components: {
    PageHeader,
    PageFooter,
    FoodCorner,
    PopularRecipes
  }
}
</script>

<template>
  <!-- Il template si divide in sections -->
  <section>
    <PageHeader />
  </section>
  <section>
    <FoodCorner />
  </section>
  <section>
    <PopularRecipes />
  </section>
  <section>
    <PageFooter />
  </section>
</template>

<style lang="scss">
@use './styles/partials/variables.scss' as *;
@use './styles/general.scss' as *;

body {
  background-color: $grigio;
  font-family: 'Times New Roman', Times, serif;
}
</style>
