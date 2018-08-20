<template>
  <div id="app">
    <app-text></app-text>
    <app-text></app-text>
    <app-text></app-text>
  </div>
</template>

<script>
import AppText from './components/app-text.vue'

export default {
  components: {
    AppText: AppText
  }
}
</script>

<style>
*, ::before, ::after { margin: 0; box-sizing: border-box; }
</style>
