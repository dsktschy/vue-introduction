<template>
  <div id="app">
    <app-modal :visible="appModalVisible"></app-modal>
  </div>
</template>

<script>
import AppModal from './components/app-modal.vue'

export default {
  components: {
    AppModal: AppModal
  },
  data: function () {
    return {
      appModalVisible: false
    }
  }
}
</script>

<style>
*, ::before, ::after { margin: 0; box-sizing: border-box; }
</style>
