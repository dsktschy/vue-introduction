<template>
  <div id="app">
    <app-modal></app-modal>
  </div>
</template>

<script>
import AppModal from './components/app-modal.vue'

export default {
  components: {
    AppModal: AppModal
  }
}
</script>

<style>
*, ::before, ::after { margin: 0; box-sizing: border-box; }
</style>
