<script setup>
import { ref } from 'vue'

const clock = ref({
  seconds1: 0,
  seconds2: 0,
  minutes1: 0,
  minutes2: 0,
  hours1: 0,
  hours2: 0
})

function constPlus() {
  clock.value.seconds1++
  if (clock.value.seconds1 > 9) {
    clock.value.seconds2++
    clock.value.seconds1 = 0
  }
  if (clock.value.seconds2 > 5) {
    clock.value.minutes1++
    clock.value.seconds2 = 0
  }
  if (clock.value.minutes1 > 9) {
    clock.value.minutes2++
    clock.value.minutes1 = 0
  }
  if (clock.value.minutes2 > 5) {
    clock.value.hours1++
    clock.value.minutes2 = 0
  }
  if (clock.value.hours1 > 9) {
    clock.value.hours2++
    clock.value.hours1 = 0
  }
}

setInterval(constPlus, 1000)
</script>

<template>
  <div>
    Таймер - {{ clock.hours2 }}{{ clock.hours1 }}:{{ clock.minutes2 }}{{ clock.minutes1 }}:{{
      clock.seconds2
    }}{{ clock.seconds1 }}
  </div>
  <button @click="">test</button>
</template>

<style scoped></style>
