<script>
// Qui va il codice JavaScript

export default {
    name: "PageHeader",
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
    <!-- Qui ci va l'HTML dell'Header del sito 'Food Corner' Top Japanese restaurants for Sushi. -->
    <header>
        <div class="header-top">

            <div class="header-top-left">
                <div>
                    <a href="">Download App</a>
                    <button>iOS</button>
                </div>
                <a href="">Advertise with us</a>


            </div>

            <div class="header-top-right">
                <a href=""><i class="fa-brands fa-facebook-f"></i></a>
                <a href=""><i class="fa-brands fa-instagram"></i></a>
                <a href=""><i class="fa-brands fa-twitter"></i></a>
                <a href=""><i class="fa-brands fa-youtube"></i></a>
            </div>
        </div>

        <div class="header-central-logo">
            <!-- Qui ci va il logo con sotto scritto AVADA FOOD -->
            <img src="../assets/avada-food-logo-2x.png" alt="">
        </div>

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
    </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

/* Questa parte di css è relativa solo a questo componente  */
header {
    width: 70%;
    margin: 0px auto;
}

.header-top {

    display: flex;
    justify-content: space-between;
    margin: 0px auto;
    font-size: 10px;
}

.header-top-right {
    width: 13%;
    display: flex;
    justify-content: space-around;
}

.header-top-left {
    width: 20%;
    display: flex;
    justify-content: space-around;
    align-items: center;
}

a {
    font-weight: 500;
    color: #67615a;
    text-decoration: inherit;
}

a:hover {
    color: #FC7523;
}

button {
    background-color: #FC7523;
    color: white;
    border: 1px solid transparent;
    cursor: pointer;
    margin-left: 5px;
    font-size: 10px;
}

.menu-list {
    width: 50%;
    margin: 0px auto;
    list-style: none;
    display: flex;
    justify-content: space-around;
    align-items: center;
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
    color: black;
}

.menu-list a:hover {
    color: #FC7523;
    text-decoration: underline;
    cursor: pointer;
}

img {
    height: 100px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%),
}

.header-central-logo {
    position: relative;
}

nav {
    margin-top: 150px;
}
</style>