<template>
  <div :class="[ 'app-common', { 'is-offset': $route.path !== '/' } ]">
    <div class="image">
      <div class="content">
        <h1 class="heading">
          <nuxt-link to="/">山田太郎・Taro YAMADA</nuxt-link>
        </h1>
        <nav>
          <ul>
            <li class="nav-item">
              <nuxt-link to="/profile" class="nav-text">略歴・Profile</nuxt-link>
            </li>
            <li class="nav-item">
              <nuxt-link to="/works" class="nav-text">実績・Works</nuxt-link>
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

<style scoped>
.app-common {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  padding: 40px;
  transition: transform .3s ease;
  &.is-offset {
    transform: translateX(-280px);
  }
}
.image {
  position: relative;
  width: 100%;
  height: 100%;
  background-image: url(~/assets/images/image-1.jpg);
  background-size: cover;
  background-position: center;
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
    transform: rotate(63deg);
    background-color: rgba(255, 0, 0, .2);
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
