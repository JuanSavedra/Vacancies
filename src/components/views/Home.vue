<template>
  <div class="container py-4">
    <div class="row">
      <div class="col">
        <SearchVacancy />
      </div>
    </div>
    <div class="row mt-5" v-for="(vacancy, index) in vacancys" v-bind:key="index">
      <div class="col">
        <Vacancy 
          v-bind:title="vacancy.title"
          v-bind:description="vacancy.description" 
          v-bind:salary="vacancy.salary" 
          v-bind:model="vacancy.model" 
          v-bind:type="vacancy.type" 
          v-bind:publicationDate="vacancy.publicationDate" 
        />
      </div>
    </div>
    <div class="row mt-5">
      <div class="col-4">
        <Indicator 
          title="Vagas abertas" 
          indicator="100" 
          bg="bg-dark" 
          color="text-white"
        />
      </div>
      <div class="col-4">
        <Indicator 
          title="Profissionais cadastrados"
          indicator="225" 
          bg="bg-dark" 
          color="text-white" 
        />
      </div>
      <div class="col-4">
        <Indicator 
          title="Visitantes online" 
          v-bind:indicator="usersOnline" 
          bg="bg-light" 
          color="text-dark" 
        />
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
      usersOnline: 0,
      vacancys: [
        {
          id: 1,
          title: 'Analista Programador PHP Pleno',
          description: 'Profissional com conhecimentos em PHP, Laravel e MySQL. Necessário 3 anos de experiências. Atuará na manutenção de sistemas legados da empresa.',
          salary: 6000,
          model: 'Home Office',
          type: 'PJ',
          publicationDate: '2021-10-10'
        },
        {
          id: 2,
          title: 'Programador JavaScript Angular',
          description: 'Profissional com conhecimentos avançados em JavaScript e Angular.',
          salary: 5000,
          model: 'Presencial',
          type: 'CLT',
          publicationDate: '2021-10-07'
        },
        {
          id: 3,
          title: 'Programador JavaScript Vue',
          description: 'Profissional com conhecimentos avançados em JavaScript e Vue.',
          salary: 5000,
          model: 'Home Office',
          type: 'CLT',
          publicationDate: '2021-10-06'
        },
        {
          id: 4,
          title: 'Analista de Banco de Dados Sênior',
          description: 'Domínio dos bancos de dados SQL Server, Oracle, Postgre e MySQL',
          salary: 9000,
          model: 'Presencial',
          type: 'PJ',
          publicationDate: '2021-10-06'
        },
        {
          id: 5,
          title: 'Programador Web Júnior',
          description: 'Conhecimentos básicos em HTML, CSS, JavaScript, Bootstrap, PHP e MySQL',
          salary: 3000,
          model: 'Presencial',
          type: 'CLT',
          publicationDate: '2021-10-05'
        }
      ]
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