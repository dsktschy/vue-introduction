<template>
  <div>
    <app-common/>
    <nuxt/>
  </div>
</template>

<script>
import AppCommon from '~/components/app-common'

export default {
  components: {
    AppCommon
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
