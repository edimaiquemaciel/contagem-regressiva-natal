<script setup>
import bola from "../assets/bola.png";
import Button from "./Button.vue";
</script>

<template>
    <section>
        <img :src="bola" alt="Bola de Natal">
        <div>
            <h2>Conectando generosidade ao redor do mundos</h2>
            <p>Celebre a magia do Natal de uma maneira especial! Descubra a plataforma que permite a doação de presentes significativos para aqueles que mais precisam. Faça parte do movimento e compartilhe o verdadeiro espírito da generosidade.</p>
            <Button />
        </div>
    </section>

</template>

<style scoped lang="scss">
section{
    display: flex;
    justify-content: space-evenly;
    align-items: center;

    div{
        text-align: left;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        gap: 15px;
        h2{
            font-size: 28px;
            width: 380px;
        }
        p{
            font-size: 18px;
            width: 420px;
            line-height: 30px;
            font-weight: 400;
            text-align: left;
            margin-bottom: 20px;  
        }
    }

    img{
        width: 330px;
    }
}

</style>