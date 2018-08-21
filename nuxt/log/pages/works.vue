<template>
  <div class="page">
    <ul class="page-inner works">
      <li
        class="works-item"
        :style="{ 'background-image': `url(/images/image-1.jpg)` }"
      >
        <pre class="works-text">Work-1</pre>
      </li>
      <li
        class="works-item"
        :style="{ 'background-image': `url(/images/image-2.jpg)` }"
      >
        <pre class="works-text">Work-2</pre>
      </li>
      <li
        class="works-item"
        :style="{ 'background-image': `url(/images/image-3.jpg)` }"
      >
        <pre class="works-text">Work-3</pre>
      </li>
    </ul>
  </div>
</template>

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
