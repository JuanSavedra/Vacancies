<template>
  <div class="container py-4">
    <div class="row">
      <div class="col">
        <SearchVacancy />
      </div>
    </div>
    <div class="row mt-5">
      <div class="col-4">
        <Indicator />
      </div>
      <div class="col-4">
        <Indicator />
      </div>
      <div class="col-4">
        <Indicator />
      </div>
    </div>
  </div>
</template>
  
<script>
  import SearchVacancy from '@/components/comuns/SearchVacancy.vue'
  import Indicator from '@/components/comuns/Indicator.vue'

  export default {
    name: 'Home',
    components: {
      SearchVacancy,
      Indicator
    },
    activated() {
      console.log("Componente ativado.")
    },
    deactivated() {
      console.log("Componente desativado.")
    }
  }
</script>
  
<style></style>