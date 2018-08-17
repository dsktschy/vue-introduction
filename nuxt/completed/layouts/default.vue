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
