<template>
  <div>
    <app-common :image="createImageUrl()"/>
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
    createImageUrl () {
      const max = 3
      const min = 1
      const number = Math.floor(Math.random() * (max + 1 - min) + min)
      return `/images/image-${number}.jpg`
    }
  }
}
</script>
