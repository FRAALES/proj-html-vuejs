<!-- Bisogna cambiare prima di tutto le cose della composition API, dato che usiamo l'options API -->
<script>
import PageHeader from './components/PageHeader.vue';

export default {
  components: {
    PageHeader,
  }
}
</script>

<template>
  <!-- Il template si divide in sections -->
  <section>
    <PageHeader />
  </section>
</template>

<style scoped></style>
