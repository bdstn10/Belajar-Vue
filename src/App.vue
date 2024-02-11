<script setup>
import HelloWorldd from '../src/components/HelloWorld.vue'
import Testing from '../src/components/Testing.vue'
import { ref,onMounted } from 'vue';
const count = ref(0)
function increment() {
  count.value++
}
onMounted(() => {
  console.log(`The initial value of 'count' state is: ${count.value}`)
})
</script>

<template>
  <Testing/>
  <button @click="increment">Count is : {{ count }}</button>
  <HelloWorldd/>
  <Testing/>
</template>

<style scoped>
  button {
    font-weight: bold;
  }
</style>
