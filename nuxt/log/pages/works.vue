<template>
  <div class="page">
    <ul class="page-inner works">
      <li
        v-for="content of appModalContents"
        :key="content.id"
        class="works-item"
        :style="{ 'background-image': `url(${content.image})` }"
        @click="openAppModal(content)"
      >
        <pre class="works-text">{{content.label}}</pre>
      </li>
    </ul>
    <app-modal
      :visible="appModalVisible"
      :image="appModalImage"
      :text="appModalText"
      @click-outside="closeAppModal"
    />
  </div>
</template>

<script>
import AppModal from '~/components/app-modal'

export default {
  components: {
    AppModal
  },
  data () {
    return {
      appModalVisible: false,
      appModalImage: '',
      appModalText: '',
      appModalContents: [
        {
          id: 'content-1',
          image: '/images/image-1.jpg',
          label: '山田花子\nオフィシャルサイト',
          text: '山田花子 オフィシャルサイト を制作しました。'
        },
        {
          id: 'content-2',
          image: '/images/image-2.jpg',
          label: '山田製薬\n社内管理ツール',
          text: '山田製薬 社内管理ツール を制作しました。'
        },
        {
          id: 'content-3',
          image: '/images/image-3.jpg',
          label: '株式会社 YAMADA\nコーポレートサイト',
          text: '株式会社 YAMADA コーポレートサイト を制作しました。'
        }
      ]
    }
  },
  methods: {
    openAppModal (content) {
      this.appModalVisible = true,
      this.appModalImage = content.image,
      this.appModalText= content.text
    },
    closeAppModal () {
      this.appModalVisible = false
    }
  }
}
</script>

<style scoped>
.works-item {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 200px;
  height: 112px;
  background-size: cover;
  background-position: center;
  margin-left: auto;
  margin-right: 0;
  cursor: pointer;
  &:not(:first-child) {
    margin-top: 30px;
  }
}
.works-text {
  line-height: 1.5;
  font-size: 12px;
  font-weight: 900;
  text-align: center;
  color: #fff;
}
</style>
