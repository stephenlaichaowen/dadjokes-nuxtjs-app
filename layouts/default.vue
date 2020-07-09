<template>
  <div class="container">
    <AppHeader />
    <nuxt />
  </div>
</template>

<script>
import AppHeader from '@/components/AppHeader'

export default {
  name: 'layout',
  components: {
    AppHeader
  }
}
</script>

