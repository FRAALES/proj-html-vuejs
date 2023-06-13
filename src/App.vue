<!-- Bisogna cambiare prima di tutto le cose della composition API, dato che usiamo l'options API -->
<script>
import PageHeader from './components/PageHeader.vue';
import PageFooter from './components/PageFooter.vue';

export default {
  components: {
    PageHeader,
    PageFooter
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
</template>

<style lang="scss">
@use './styles/partials/variables.scss' as *;
@use './styles/general.scss' as *;
</style>
