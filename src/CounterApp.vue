<template>
  <div class="container">
    <h1>🔢 Counter App</h1>
    <p class="count">{{ count }}</p>
    <div class="buttons">
      <button @click="decrease" :disabled="count === 0">-</button>
      <button @click="reset">Reset</button>
      <button @click="increase">+</button>
    </div>
  </div>
</template>

<script setup>
import {ref} from 'vue';

const count = ref(0);

const increase = () => {
  count.value++;
}

const decrease = () => {
  if (count.value > 0) {
    count.value--;
  }
}

const reset = () => {
  count.value = 0;
}

</script>