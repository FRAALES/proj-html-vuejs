<script>
export default {
    name: "BottomPictures",
}
</script>

<template>
    <div class="unicodiv">
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

.unicodiv {
    display: inline-block;

    img {
        width: calc(100% / 4);
    }
}
</style>