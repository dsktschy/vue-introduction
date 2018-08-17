<template>
  <transition>
    <div
      class="app-modal"
      v-show="visible"
      @click.self="$emit('click-outside')"
    >
      <div
        class="image"
        :style="{ 'background-image': `url(${image})` }"
      >
        <p class="text">
          {{text}}
        </p>
      </div>
    </div>
  </transition>
</template>

<script>
export default {
  props: [
    'visible',
    'image',
    'text'
  ]
}
</script>

<style scoped>
.app-modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 10;
  background-color: rgba(0, 0, 0, .7);
}
.app-modal.v-enter-active { transition: opacity .1s linear; }
.app-modal.v-enter        { opacity: 0; }
.app-modal.v-enter-to     { opacity: 1; }
.app-modal.v-leave-active { transition: opacity .4s linear; }
.app-modal.v-leave        { opacity: 1; }
.app-modal.v-leave-to     { opacity: 0; }
.image {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  display: block;
  width: 80vw;
  height: 80vh;
  background-size: cover;
  background-position: center;
}
.text {
  position: absolute;
  bottom: 36px;
  right: 40px;
  line-height: 1.5;
  font-size: 16px;
  font-weight: 900;
  text-align: right;
  color: #fff;
}
</style>
