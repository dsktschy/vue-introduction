<template>
  <section class="page-profile">
    <div class="inner">
      <h2 class="heading">山田太郎・Taro YAMADA</h2>
      <p class="paragraph">
        名古屋を中心に活動するエンジニアです<br>
        Webサイト制作からWebサービス開発まで<br>
        Webのフロントエンド領域を幅広くカバーします
      </p>
      <p class="paragraph">
        2012年より東京のWeb制作会社に勤務<br>
        2016年に独立、名古屋に拠点を移す
      </p>
      <p class="paragraph">
        使用技術<br>
        HTML・CSS・JavaScript<br>
        Pug・SCSS・ES20XX<br>
        jQuery・Bootstrap・Vue.js・Nuxt.js<br>
        NodeJS・PHP・Python<br>
        Express・Laravel・Django
      </p>
    </div>
  </section>
</template>

<style scoped>
.page-profile {
  width: 280px;
  height: 100vh;
  margin-left: auto;
  margin-right: 0;
  padding: 40px 40px 40px 0;
  display: flex;
  align-items: center;
}
.inner {
  width: 100%;
  max-height: 100%;
  overflow: hidden auto;
  text-align: right;
}
.heading {
  line-height: 1.5;
  font-size: 16px;
  font-weight: 900;
}
.paragraph {
  line-height: 1.5;
  font-size: 10px;
  font-weight: 900;
  margin-top: 18px;
  &:first-child {
    margin-top: 40px;
  }
}
</style>
