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
    <footer>
        <div class="footer-left-left">
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

        <nav>
            <ul class="menu-list">
                <!-- Iterazione delle voci di menù e rendering dinamico -->
                <li v-for="menuItem in menuItems" :key="menuItem.id">
                    <a :href="menuItem.url">{{ menuItem.label }}</a>
                </li>
            </ul>
        </nav>

        <hr>

        <div>
            <h4>CONTACT</h4>
            <div class="d-flex">
                <div>
                    <i class="fa-sharp fa-solid fa-location-dot"></i>
                </div>
                <div>
                    <p>775 New York Ave, Brooklyn, Kings, New York 11203</p>
                </div>
            </div>

            <div class="d-flex">
                <div>
                    <i class="fa-solid fa-phone-flip"></i>
                </div>
                <div>
                    <p>+0100-505-0000</p>
                </div>
            </div>

            <div class="d-flex">
                <div>
                    <i class="fa-solid fa-envelope"></i>
                </div>
                <div>
                    <p>info@your-domain.com</p>
                </div>
            </div>
        </div>

        <hr>

        <div>
            <h4>GET OUR APP!</h4>
            <div class="rettangolo d-flex">
                <div>
                    <i class="fa-solid fa-play"></i>
                </div>
                <div>
                    <h5>GET IT ON</h5>
                    <h3>Google Play</h3>
                </div>
            </div>

            <div class="rettangolo d-flex">
                <div>
                    <i class="fa-brands fa-apple"></i>
                </div>
                <div>
                    <h5>Download on the</h5>
                    <h3>App Store</h3>
                </div>
            </div>
        </div>


    </footer>
</template>


<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

/* Questa parte di css è relativa solo a questo componente  */
footer {
    width: 70%;
    display: flex;
    justify-content: space-between;
    margin: 50px auto;


    .footer-left-left-bottom a {
        margin-top: 30px;
        color: $grigioscuro;
    }
}

a:hover {
    color: $arancione;
    text-decoration: underline;
    cursor: pointer;
}

.menu-list {
    width: 50%;
    margin: 0px auto;
    list-style: none;
    padding: 0;
}

.menu-list li {
    margin-right: 10px;
}

.menu-list li:last-child {
    margin-right: 0;
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
    color: #F5F5F1;
}

.footer-left-left-bottom {
    width: 100%;
    display: flex;
    justify-content: space-around;
}
</style>