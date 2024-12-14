<script setup>
import Countdown from './Countdown.vue';
import Donation from './Donation.vue';
</script>

<template>
    <main>
        <Countdown />
        <Donation />
    </main>
    
</template>

<style scoped lang="scss">
main{
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    gap: 100px;
}
</style>