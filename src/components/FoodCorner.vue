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

    <div class="box-bianco">
        <h3>
            FOODIE JOURNAL
        </h3>
        <div class="cards-container">
            <!-- Questa è la prima card -->
            <div class="card">
                <div class="picture">
                    <img src="../assets/single-post-img3-200x132.jpg" alt="">
                </div>
                <div class="didascalia">
                    <div class="titolo-didascalia">
                        <h3> Food Corner: Top Japanese Restaurants for Sushi</h3>
                    </div>
                    <div class="signature-didascalia">
                        By admin | March 25th, 2019
                    </div>
                </div>
            </div>

            <!-- Questa è la seconda card -->
            <div class="card">
                <div class="picture">
                    <img src="../assets/fi-roundup-200x132.jpg" alt="">
                </div>
                <div class="didascalia">
                    <div class="titolo-didascalia">
                        <h3>Roundup: My New Favourite Recipes For Healthy Living</h3>
                    </div>
                    <div class="signature-didascalia">
                        By admin | March 25th, 2019
                    </div>
                </div>
            </div>

            <!-- Questa è la terza card -->
            <div class="card">
                <div class="picture">
                    <img src="../assets/fi-toasts-200x132.jpg" alt="">
                </div>
                <div class="didascalia">
                    <div class="titolo-didascalia">
                        <h3>Why These Toasts with Tea are My New Favourite</h3>
                    </div>
                    <div class="signature-didascalia">
                        By admin | March 25th, 2019
                    </div>
                </div>
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

// Qui inizia il css del cards-container
.box-bianco {
    width: 60%;
    margin: -50px auto 100px;
    background-color: white;
    padding: 30px;

    h3 {
        text-align: center;
        margin: 0 auto 15px;
        color: $grigioscuro;
    }
}

.cards-container {
    display: flex;
}

.card {
    width: calc(100% / 3);

    .didascalia {
        text-align: center;
        max-width: 85%;
    }

    .signature-didascalia {
        font-size: 13px;
        color: $grigioscuro;
    }
}</style>