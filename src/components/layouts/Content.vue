<template>
  <div>
    <h1>Content</h1>
    <Home />
    <PublishVacancy />
  </div>
</template>
  
<script>
  import Home from '@/components/views/Home.vue'
  import PublishVacancy from '@/components/views/PublishVacancy.vue'

  export default {
    name: 'Content',
    components: {
      Home,
      PublishVacancy
    }
  }
</script>
  
<style></style>