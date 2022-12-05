<template>
  <div>
    <h1>Content</h1>
    <button v-on:click="content = 'Home'">Home</button>
    <button v-on:click="content = 'PublishVacancy'">Publicar Vaga</button>
    <keep-alive>
      <component v-bind:is="content" />
    </keep-alive>
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
    },
    data: () => ({
      content: 'Home'
    })
  }
</script>
  
<style></style>