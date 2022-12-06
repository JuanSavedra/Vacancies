<template>
  <div class="container py-4">
    <div class="row">
      <div class="col">
        <SearchVacancy />
      </div>
    </div>

    <div class="row mt-5">
      <div class="col">
        <Vacancy />
      </div>
    </div>

    <div class="row mt-5">
      <div class="col-4">
        <Indicator title="Vagas abertas" indicator="100" bg="bg-dark" color="text-white"/>
      </div>
      <div class="col-4">
        <Indicator title="Profissionais cadastrados" indicator="225" bg="bg-dark" color="text-white" />
      </div>
      <div class="col-4">
        <Indicator title="Visitantes online" v-bind:indicator="usersOnline" bg="bg-light" color="text-dark" />
      </div>
    </div>
  </div>
</template>
  
<script>
  import SearchVacancy from '@/components/comuns/SearchVacancy.vue'
  import Indicator from '@/components/comuns/Indicator.vue'
  import Vacancy from '@/components/comuns/Vacancy.vue'

  export default {
    name: 'Home',
    components: {
      SearchVacancy,
      Indicator,
      Vacancy
    },
    data: () => ({
      usersOnline: 0
    }),
    methods: {
      getUsersOnline() {
        this.usersOnline = Math.floor(Math.random() * 101)
      }
    },
    created() {
      setInterval(this.getUsersOnline, 1000)
    },
  }
</script>
  
<style></style>