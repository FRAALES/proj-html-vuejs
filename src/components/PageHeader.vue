<script>
    // Qui va il codice JavaScript

    export default {
        name: "PageHeader",
    }

    defineProps({
        msg: String,
    })

</script>

<template>
    <!-- Il template si divide in sections -->
    <h1>{{ YO }}</h1>

    <div class="card">
        <button type="button" @click="count++">count is {{ count }}</button>
        <p>
            Edit
            <code>components/HelloWorld.vue</code> to test HMR
        </p>
    </div>

    <p>
        Check out
        <a href="https://vuejs.org/guide/quick-start.html#local" target="_blank">create-vue</a>, the official Vue + Vite
        starter
    </p>
    <p>
        Install
        <a href="https://github.com/vuejs/language-tools" target="_blank">Volar</a>
        in your IDE for a better DX
    </p>
    <p class="read-the-docs">Click on the Vite and Vue logos to learn more</p>
</template>

<style scoped>
    /* Questa parte di css è relativa solo a questo componente  */
    .read-the-docs {
        color: #888;
    }
</style>