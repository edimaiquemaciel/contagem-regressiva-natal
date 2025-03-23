<script setup>
import presente from "../assets/presente.png";
import { ref, onMounted, onUnmounted } from 'vue';
import moment from 'moment';
import NumberFlow  from "@number-flow/vue";

const now = ref(moment());
const christmas = moment('December 25, 2025, 00:00:00', 'MMMM DD, YYYY, HH:mm:ss');
const mensagemNatal = ref('');

const countdownParts = ref({
  days: 0,
  hours: 0,
  minutes: 0,
  seconds: 0
});

function updateCountdown() {
    const duration = moment.duration(christmas.diff(now.value));
    if(duration.asSeconds() > 0){
      countdownParts.value = {
        days: duration.days(),
        hours: duration.hours(),
        minutes: duration.minutes(),
        seconds: duration.seconds()
      };
    }else{
      mensagemNatal.value = "🎄🎅Feliz Natal!!🎅🎄";
    }
    

}


onMounted(() => {
    updateCountdown();
    const interval = setInterval(() => {
      now.value = moment();
      updateCountdown();
    }, 1000);

    onUnmounted(() => clearInterval(interval));
});
</script>

<template>
  <section>
    <h2>Tempo limitado</h2>
    <p>Nessas festas de fim de ano mande um presente para a pessoa amada e compartilhe a alegria do Natal.</p>
    <div class="contador">
        <div class="countdown-item">
           <NumberFlow :value="countdownParts.days" suffix="d - "/>
        </div>
        <div class="countdown-item">
            <NumberFlow :value="countdownParts.hours" suffix="h - "/>
        </div>
        <div class="countdown-item">
            <NumberFlow :value="countdownParts.minutes" suffix="m - "/>
        </div>
        <div class="countdown-item">
            <NumberFlow :value="countdownParts.seconds" suffix="s"/>
        </div>
    </div>
    <p v-if="mensagemNatal">{{ mensagemNatal }}</p>
    <img :src="presente" alt="Presente de Natal">
  </section>
</template>

<style scoped>
section {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  h2 {
  font-size: 30px;
  margin-bottom: 15px;
}

p {
  font-size: 16px;
  width: 380px;
  line-height: 25px;
  margin-bottom: 20px;
}

.contador {
  display: flex;
  justify-content: center;
  align-items: center;
}

.countdown-group {
  display: flex;
  gap: 20px;
}
  
number-flow-vue::part(number),
number-flow-vue::part(suffix) {
  line-height: 1.7;
  font-size: 60px;
  color: #CD3C32;
  font-weight: 600;

}
img{
  width: 400px;
}

}
</style>
