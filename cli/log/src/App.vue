<template>
  <div id="app">
    <button
      v-for="content of appModalContents"
      :key="content.id"
      @click="openAppModal(content)"
    >
      {{content.text}}
    </button>
    <app-modal
      :visible="appModalVisible"
      :image="appModalImage"
      :text="appModalText"
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
      appModalVisible: false,
      appModalImage: '',
      appModalText: '',
      appModalContents: [
        { id: 'content-1', image: '/images/image-1.jpg', text: 'Image-1' },
        { id: 'content-2', image: '/images/image-2.jpg', text: 'Image-2' },
        { id: 'content-3', image: '/images/image-3.jpg', text: 'Image-3' }
      ]
    }
  },
  methods: {
    openAppModal: function (content) {
      this.appModalVisible = true
      this.appModalImage = content.image
      this.appModalText = content.text
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
