<script setup>
import { ref } from 'vue';

const count = ref(0);

function increment(){
  count.value++;
}
</script>

<template>
  <h1>HELLO WORLD</h1>
  <img src="/images/pixelpfp.jpg">
  <button @click="increment">{{count}}</button>
</template>

<style lang="scss">
@use './styles/abstracts' as *;
@use './styles/resets.scss';

h1{
  color: $color-main;
}

button{
  padding: 2rem;
  background-color: $color-main;
  color: white;
}

</style>
