<script setup>
import Header  from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";
</script>

<template>
    <body>
        <Header />
        <Main />
        <Footer />
    </body>
</template>

<style scoped lang="scss">
body{
    font-family: "Archivo", sans-serif;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    min-height: 100vh;
    gap: 100px;
}

</style>
