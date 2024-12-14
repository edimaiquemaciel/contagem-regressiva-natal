<script setup>
import LogoNoel from "./LogoNoel.vue";
import loja from "../assets/loja.png";
import Button from "./Button.vue";
</script>

<template>
    <header>
        <section>
            <LogoNoel />
            <h1>Uma <span>plataforma de doação</span> para espalhar alegria</h1>
            <div>
              <p>Nessas festas de fim de ano mande um presente</p>
              <p>para a pessoa amada e compartilhe a alegria do Natal.</p>
            </div>
            <Button/>
        </section>
        <img class="loja-img" :src="loja" alt="Frente de Loja">
    </header>
</template>

<style scoped>
header{
    background-color: #FFE9E8;
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    height: 55vh;
    padding: 0 40px;

    section{
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      justify-content: space-between;
      gap: 25px;

      h1{
      font-size: 30px;
      width: 450px;
      }
      span{
        color: #CD3C32;
      }
      p{
        font-size: 19px;
        margin-bottom: 10px;
      }
    }

    .loja-img{
      width: 380px;
    }
    
    
}
</style>