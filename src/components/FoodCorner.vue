<script>
export default {
    name: "FoodCorner",
}
</script>


<template>
    <div class="immagine-grande">
        <div class="rettangolo-centrale">
            <div class="box-arancione">
                <h5>TODAY'S PICK</h5>
            </div>
            <div>
                <h1>
                    Food Corner: Top Japanese Restaurants for Sushi
                </h1>
                <p class="data">
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
    background-image: url("../assets/single-post-img3-600x395.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    height: 500px;
    width: 100%;
    display: flex;
    align-items: center;
    margin-top: 20px;
}


.rettangolo-centrale {
    background-color: white;
    width: 80%;
    max-width: 600px;
    border-radius: 10px;
    margin: 0 auto;
    padding: 40px;
    text-align: center;
    position: relative;
}

.box-arancione {
    background-color: $arancione;
    display: inline-block;
    padding: 10px;
    position: absolute;
    top: -20px;
    left: 50%;
    transform: translateX(-50%);
    color: white;
}

.rettangolo-centrale h1 {
    margin: 0;
    font-size: 34px;
}

.data {
    margin-top: 10px;
    color: $grigioscuro;
}
</style>