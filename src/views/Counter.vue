<script>
import {defineComponent, ref} from 'vue'
import useCounter from "@/composables/useCounter";

export default defineComponent({
  name: "Counter",
  //props: {} anirien aquí
  //emits: [] aniria aquí
  setup() {

    const {counter, increase, decrease} = useCounter(25)

    return{
      counter,
      increase,
      decrease
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