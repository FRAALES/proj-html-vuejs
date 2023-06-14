<script>
export default {
    name: "FoodCorner",
}
</script>


<template>
    <div class="immagine-grande">
        <div>
            <h1>
                Food Corner: Top Japanese Restaurants for Sushi
            </h1>
            <p>
                March 25, 2019
            </p>
        </div>

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

.immagine-grande {
    width: 100%;
    background-image: url("single-post-img3-600x395.jpg");
}
</style>