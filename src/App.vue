<!-- Dibawah merupakan contoh penggunaan Options API pada logika component Vue -->
<script>
export default {
  // Properties returned from data() become reactive state 
  // and will be exposed on 'this'.
  data() {
    return {
      count: 0
    }
  },

  // Methods are functions that mutate state and trigger updates.
  // They can be bound as event handler in template
  methods: {
    increment() {
      this.count++
    }
  },

  // Lifecycle hooks are called at different stages 
  // of a component's lifecycle.
  // This function will be called when the component is mounted
  mounted() {
    console.log(`The initial value of count state is ${this.count}`)
  }
}
</script>

<template>
  <button @click="increment">Count is : {{ count }}</button>
</template>

<style scoped>
  button {
    font-weight: bold;
  }
</style>
