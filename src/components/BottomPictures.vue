<script>
export default {
    name: "BottomPictures",
}
</script>

<template>
    <div class="img-container">
        <img src="../assets/Yogurt-Nan-400x263.jpg" alt="">
        <img src="../assets/Mixed-fruits-400x263.jpg" alt="">
        <img src="../assets/fi-korean-food-400x263.jpg" alt="">
        <img src="../assets/r-michelle-tsang-500721-unsplash-min-400x263.jpg" alt="">
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

/* Questa parte di css è relativa solo a questo componente  */
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

.img-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;

    img {
        width: calc(100% / 4);
        height: auto;
        max-width: 100%;
        max-height: 100%;
        object-fit: cover;
    }
}
</style>