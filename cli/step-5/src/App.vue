<template>
  <div id="app">
    <button @click="openAppModal">Open</button>
    <app-modal
      :visible="appModalVisible"
      @click-outside="closeAppModal"
    ></app-modal>
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
  },
  methods: {
    openAppModal: function () {
      this.appModalVisible = true
    },
    closeAppModal: function () {
      this.appModalVisible = false
    }
  }
}
</script>

<style>
*, ::before, ::after { margin: 0; box-sizing: border-box; }
</style>
