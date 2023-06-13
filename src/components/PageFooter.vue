<script>
// Qui va il codice JavaScript

export default {
    name: "PageFooter",
    data() {
        return {
            menuItems: [
                { id: 1, label: 'Home' },
                { id: 2, label: 'Recipes' },
                { id: 3, label: 'Places' },
                { id: 4, label: 'Blog' },
                { id: 5, label: 'About' },
                { id: 6, label: 'Contact' },
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
                <li>
                    <a href=""><i class="fa-solid fa-magnifying-glass"></i></a>
                </li>
            </ul>
        </nav>


    </footer>
</template>


<style scoped>
/* Questa parte di css è relativa solo a questo componente  */
footer {
    width: 70%;
    margin-top: 20px;
    display: flex;
    margin: 0 auto;
}

.menu-list {
    width: 50%;
    margin: 0px auto;
    list-style: none;


    padding: 0;
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