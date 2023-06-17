<script setup>
import Timer from './components/Timer.vue'
import Form from './components/Form.vue'
</script>

<template>
  <Timer></Timer>
  <div class="gg" v-for="i in 5">
    <ul>
      <li> Текст <Form /></li>
    </ul>
  </div>
</template>

<style>
@import './assets/styles.css';
</style>
