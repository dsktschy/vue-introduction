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
*, *:before, *:after {
  box-sizing: border-box;
  margin: 0;
  font-family: 'Noto Sans Japanese', sans-serif;
}
html {
  font-size: 16px;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
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
