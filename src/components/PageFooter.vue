<script>
// Qui va il codice JavaScript

export default {
    name: "PageFooter",
    data() {
        return {
            menuItems: [
                { id: 1, label: 'Recipes' },
                { id: 2, label: 'Places' },
                { id: 3, label: 'Blog' },
                { id: 4, label: 'About' },
                { id: 5, label: 'Contact' },
                // Qui si possono aggiungere altre voci di menù se necessario, a seconda delle esigenze future
            ]
        };
    }
}

// defineProps({
//     msg: String,
// })

</script>


<template>
    <!-- Qui ci va l'HTML del Footer del sito 'Food Corner' Top Japanese restaurants for Sushi. -->
    <div class="footer-container">
        <footer>
            <div class="footer-left-left percent">
                <div class="footer-left-left-top">
                    <!-- Qui ci va il logo con sotto scritto AVADA FOOD -->
                    <img src="../assets/avada-food-logo-mob-2x.png" alt="">
                </div>

                <div class="footer-left-left-bottom">
                    <a href=""><i class="fa-brands fa-facebook-f"></i></a>
                    <a href=""><i class="fa-brands fa-instagram"></i></a>
                    <a href=""><i class="fa-brands fa-twitter"></i></a>
                    <a href=""><i class="fa-brands fa-youtube"></i></a>
                </div>
            </div>

            <hr>

            <nav class="percent">
                <ul class="menu-list">
                    <!-- Iterazione delle voci di menù e rendering dinamico -->
                    <li v-for="menuItem in menuItems" :key="menuItem.id">
                        <a :href="menuItem.url">{{ menuItem.label }}</a>
                    </li>
                </ul>
            </nav>

            <hr>

            <div class="percent footer-right">
                <h4>CONTACT</h4>
                <div class="d-flex">
                    <div class="icone-footer">
                        <i class="fa-sharp fa-solid fa-location-dot"></i>
                    </div>
                    <div>
                        <p>775 New York Ave, Brooklyn, Kings, New York 11203</p>
                    </div>
                </div>

                <div class="d-flex">
                    <div class="icone-footer">
                        <i class="fa-solid fa-phone-flip"></i>
                    </div>
                    <div>
                        <p>+0100-505-0000</p>
                    </div>
                </div>

                <div class="d-flex">
                    <div class="icone-footer">
                        <i class="fa-solid fa-envelope"></i>
                    </div>
                    <div>
                        <p>info@your-domain.com</p>
                    </div>
                </div>
            </div>

            <hr>

            <div class="percent footer-right">
                <h4>GET OUR APP!</h4>
                <!-- Primo bottone -->
                <img src="../assets/download-android.png" alt="">

                <!-- Secondo bottone -->
                <img src="../assets/download-app-store.png" alt="">
            </div>
        </footer>
    </div>

    <section class="bottom">
        <hr>
        <p class="copyright">
            <span class="c">
                C
            </span>
            <span>
                Copyright 2012 - 2020 | Avada Theme by ThemeFusion | All Rights Reserved | Powered by WordPress
            </span>
        </p>
    </section>
</template>


<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

/* Questa parte di css è relativa solo a questo componente  */
.footer-container {
    background-color: white;
    height: 350px;
    padding: 40px 0;
}

footer {
    width: 70%;
    display: flex;
    justify-content: space-between;
    margin: 50px auto;


    .footer-left-left-bottom a {
        margin-top: 30px;
        color: $grigioscuro;
    }

    img {
        width: 200px;
    }
}

a:hover {
    color: $arancione;
    text-decoration: underline;
    cursor: pointer;
}

.menu-list {
    width: 50%;
    height: 80%;
    margin: 20px auto;
    list-style: none;
    padding: 0;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}

.menu-list a {
    text-decoration: none;
    color: $grigioscuro;
}

.menu-list a:hover {
    color: $arancione;
    text-decoration: underline;
    cursor: pointer;
}


hr {
    color: $grigio;
}

.footer-left-left-bottom {
    width: 100%;
    display: flex;
    justify-content: flex-start;

    a {
        margin-right: 10px;

        hover {
            color: $arancione;
        }
    }
}

.percent {
    width: 25%;
}

h4 {
    color: $arancione;
}

.footer-right {
    margin-left: 30px;
    color: $grigioscuro;
}

.icone-footer {
    margin: 20px;
}

.icone-footer-right-right {
    font-size: 80px;
    margin-right: 20px;
    padding-bottom: 5px;
}

button {
    color: $grigioscuro;
    background-color: white;
    border-radius: 10px;
    border: 2px solid;
    margin-bottom: 20px;
    height: 30%;
    width: 100%;


    :hover {
        cursor: pointer;
        color: $arancione;
    }

    h3 {
        font-size: 20px;
    }
}


//Qui iniziano le regole dell'ultimo pezzettino in fondo

.bottom {
    background-color: $grigio;
    color: $grigioscuro;
    height: 100px;
    width: 100%;
    font-size: 15px;
}

.copyright {
    margin: 30px auto;
    width: 50%;
}

.c {
    border-radius: 100%;
    border: 1px solid;
    margin: 0 3px;
    padding-left: 3px;
    padding-top: 1px;
}
</style>