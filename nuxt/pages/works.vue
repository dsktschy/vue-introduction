<template>
  <div class="page">
    <ul class="page-inner works">
      <li
        class="works-item"
        @click="openAppModal({
          image: '/images/image-1.jpg',
          text: '山田花子 オフィシャルサイト を制作しました。'
        })"
      >
        <p class="works-text">
          山田花子<br>
          オフィシャルサイト
        </p>
      </li>
      <li
        class="works-item"
        @click="openAppModal({
          image: '/images/image-2.jpg',
          text: '山田製薬 社内管理ツール を制作しました。'
        })"
      >
        <p class="works-text">
          山田製薬<br>
          社内管理ツール
        </p>
      </li>
      <li
        class="works-item"
        @click="openAppModal({
          image: '/images/image-3.jpg',
          text: '株式会社 YAMADA コーポレートサイト を制作しました。'
        })"
      >
        <p class="works-text">
          株式会社 YAMADA<br>
          コーポレートサイト
        </p>
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
      appModalText: ''
    }
  },
  methods: {
    openAppModal ({ image, text }) {
      this.appModalVisible = true,
      this.appModalImage = image,
      this.appModalText= text
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
  &:nth-child(1) {
    background-image: url(/images/image-1.jpg);
  }
  &:nth-child(2) {
    background-image: url(/images/image-2.jpg);
  }
  &:nth-child(3) {
    background-image: url(/images/image-3.jpg);
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
