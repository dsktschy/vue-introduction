<template>
  <div class="page">
    <ul class="page-inner works">
      <li class="works-item">
        <p class="works-text">
          山田花子<br>
          オフィシャルサイト
        </p>
      </li>
      <li class="works-item">
        <p class="works-text">
          山田製薬<br>
          社内管理ツール
        </p>
      </li>
      <li class="works-item">
        <p class="works-text">
          株式会社 YAMADA<br>
          コーポレートサイト
        </p>
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
  &:nth-child(1) {
    background-image: url(~/assets/images/image-1.jpg);
  }
  &:nth-child(2) {
    background-image: url(~/assets/images/image-2.jpg);
  }
  &:nth-child(3) {
    background-image: url(~/assets/images/image-3.jpg);
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
