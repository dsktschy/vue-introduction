<template>
  <div class="app-modal">
    <div class="image">
      <p class="text">
        {{text}}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      text: 'Hello world!'
    }
  }
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
  background-image: url(/images/image-1.jpg);
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
