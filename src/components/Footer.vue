<script setup>
import LogoNoel from "./LogoNoel.vue";
import facebook from "../assets/logo-facebook.png";
import google from "../assets/logo-google.png";
import instagram from "../assets/logo-instagram.png";
import twitter from "../assets/logo-twitter.png";
import whatsapp from "../assets/logo-whatsapp.png";
</script>

<template>
    <footer>
        <LogoNoel />
        <div>
            <img :src="twitter" alt="Twitter">
            <img :src="whatsapp" alt="Whatsapp">
            <img :src="instagram" alt="Instagram">
            <img :src="facebook" alt="Facebook">
            <img :src="google" alt="Google">
        </div>
    </footer>
</template>

<style scoped>
footer{
    display: flex;
    justify-content: space-around;
    align-items: center;
    gap: 120px;
    height: 10vh;
    background-color: #FFE9E8;

    div{
        display: flex;
        gap: 30px;
        img{
            width: 30px;
            cursor: pointer;
        }
    }
}
</style>