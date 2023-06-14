<script>
export default {
    name: "FoodCorner",
}
</script>


<template>
    <div class="immagine-grande">
        <div class="rettangolo-centrale">
            <div class="titolo-centrale">
                <h1>
                    Food Corner: Top Japanese Restaurants for Sushi
                </h1>
                <p>
                    March 25, 2019
                </p>
            </div>
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
    height: 500px;
    background-image: url("../assets/single-post-img3-600x395.jpg");
    margin-top: 20px;
    background-position: center;
    background-size: cover;
    padding: 100px 200px;
    position: relative;

    .rettangolo-centrale {
        background-color: white;
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 600px;
        height: 200px;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        border-radius: 10px;
        padding: 50px;

        .titolo-centrale {
            width: 80%;
        }
    }
}
</style>