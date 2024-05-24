<template>
    <div class="counter">
        <button @click="decrement"> - </button>

        <span> Current value: {{ count }} </span>

        <button @click="increment"> + </button>
    </div>
</template>

<script setup>
import { ref } from 'vue';
import CounterButton from "./CounterButton.vue";
import CounterValue from "./CounterValue.vue";
import DemoContainer from '../components/DemoContainer.vue';

const count = ref(0)

/* Метод уменьшения значения */
const decrement = () => {
  count.value = count.value - 1
}

/* Метод увеличения значения */
const increment = () => {
  count.value = count.value + 1
}
</script>

<style lang="scss" scoped>
.counter {
  display: flex;
  align-items: center;
}
</style>
