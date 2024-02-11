<!-- Dibawah merupakan contoh penggunaan Composition API pada logika component Vue -->
<script setup>
import { ref,onMounted } from 'vue';

// reactive state
const count = ref(0)

// function that mutate state and trigger update
function increment() {
  count.value++
}

// lifecycle hooks
onMounted(() => {
  console.log(`The initial value of 'count' state is: ${count.value}`)
})
</script>

<template>
  <button @click="increment">Count is : {{ count }}</button>
</template>

<style scoped>
  button {
    font-weight: bold;
  }
</style>
