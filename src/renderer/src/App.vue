<script setup>
import Versions from './components/Versions.vue'
import Timer from './components/Timer.vue'
import Form from './components/Form.vue'
</script>

<template>
  <Timer></Timer>
  <div class="gg" style="flex-direction: row;" v-for="i in 5">
    <ul>
      <li> Текст <Form /></li>
    </ul>
  </div>
</template>

<style lang="less">
@import './assets/css/styles.less';
</style>
