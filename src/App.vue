<template>
  <div>
    <Navbar />
    <Content />
  </div>
</template>

<script>
import Content from '@/components/layouts/Content.vue'
import Navbar from '@/components/layouts/Navbar.vue'

export default {
  name: 'App',
  components: {
    Content,
    Navbar
  }
}
</script>

<style></style>
