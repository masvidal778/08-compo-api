<script>
import {defineComponent, ref} from 'vue'

export default defineComponent({
  name: "Counter",
  //props: {} anirien aquí
  //emits: [] aniria aquí
  setup() {

    //ref embolcalla la variable en un objecte reactiu, par això el value
    const counter = ref(5)

    return {
      counter,
      increase: () => counter.value++,
      decrease: () => counter.value--
    }

  }
})
</script>

<template>
<h1>Counter View</h1>
  <h2>{{ counter }}</h2>

  <button @click="increase">+1</button>
  <button @click="decrease">-1</button>
</template>

<style scoped>

</style>