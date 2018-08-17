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
  background-color: rgba(255, 255, 255, .7);
  &.v-enter-active { transition: opacity .2s linear; }
  &.v-enter        { opacity: 0; }
  &.v-enter-to     { opacity: 1; }
  &.v-leave-active { transition: opacity .4s linear; }
  &.v-leave        { opacity: 1; }
  &.v-leave-to     { opacity: 0; }
}
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
