<template>
  <div :class="[ 'app-common', { 'app-common-offset': $route.path !== '/' } ]">
    <div :class="[ 'image', `image-${imageNumber}` ]">
      <div class="content">
        <h1 class="heading">
          <nuxt-link to="/">山田太郎・Taro YAMADA</nuxt-link>
        </h1>
        <nav>
          <ul>
            <li class="nav-item">
              <nuxt-link to="/profile" class="nav-text">プロフィール・Profile</nuxt-link>
            </li>
            <li class="nav-item">
              <nuxt-link to="/works" class="nav-text">制作実績・Works</nuxt-link>
            </li>
            <li class="nav-item">
              <nuxt-link to="/contact" class="nav-text">お問い合わせ・Contact</nuxt-link>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    imageNumber: { type: Number, default: 1 }
  }
}
</script>

<style scoped>
.app-common {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  padding: 40px;
  transition: transform .6s cubic-bezier(0.075, 0.82, 0.165, 1);
}
.app-common-offset {
  transform: translate3d(-280px, 0, 0);
}
.image {
  position: relative;
  width: 100%;
  height: 100%;
  background-size: cover;
  background-position: center;
}
.image-1 {
  background-image: url(/images/image-1.jpg);
}
.image-2 {
  background-image: url(/images/image-2.jpg);
}
.image-3 {
  background-image: url(/images/image-3.jpg);
}
.content {
  position: absolute;
  top: 50%;
  right: 0;
  transform: translateY(-50%);
  width: 100%;
  padding-right: 40px;
  &::before {
    content: '';
    position: absolute;
    top: -30px;
    right: 180px;
    display: block;
    width: 80px;
    height: 80px;
    background-color: rgba(255, 0, 0, .2);
    animation: rotation 10s cubic-bezier(0.075, 0.82, 0.165, 1) 0s infinite;
  }
}
.heading {
  position: relative;
  z-index: 1;
  height: 40px;
  line-height: 1;
  font-size: 28px;
  font-weight: 100;
  text-align: right;
  color: #fff;
  border-bottom: 1px solid #fff;
}
.nav-item {
  margin-top: 11px;
  line-height: 1;
  font-size: 16px;
  font-weight: 100;
  color: #fff;
  text-align: right;
}
.nav-text {
  &:hover,
  &.nuxt-link-active {
    font-weight: 900;
  }
}
</style>
