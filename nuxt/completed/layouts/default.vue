<template>
  <div>
    <app-common :image-number="createImageNumber()"/>
    <nuxt/>
  </div>
</template>

<script>
import AppCommon from '~/components/app-common'

export default {
  components: {
    AppCommon
  },
  methods: {
    createImageNumber () {
      const max = 3
      const min = 1
      return Math.floor(Math.random() * (max + 1 - min) + min)
    }
  }
}
</script>

<style>
html
{
  font-family: 'Noto Sans Japanese', sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}
*, *:before, *:after
{
  box-sizing: border-box;
  margin: 0;
}
ul {
  list-style: none;
  padding: 0;
}
a {
  text-decoration: none;
  color: inherit;
}
</style>
