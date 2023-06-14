<script>
export default {
    name: "PopularRecipes",
}
</script>

<template>
    <div class="unicodiv">
        <h3>
            POPULAR RECIPES
        </h3>
        <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Error, ratione. Aspernatur rem sequi aperiam ratione,
            harum sunt ullam.
        </p>
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
    color: $grigioscuro;
}

.unicodiv {
    text-align: center;

    h3 {
        margin: 30px;
    }

    p {
        width: 40%;
        margin: 0 auto 50px;
    }
}
</style>