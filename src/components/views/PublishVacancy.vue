<template>
  <div class="container py-4">
    <div class="row">
      <div class="col">
        <h4>Apresente a sua vaga para milhares de profissionais</h4>
      </div>
    </div>
    <div class="row mt-3">
      <div class="col">
        <label class="form-label">Título da vaga</label>
        <input class="form-control" type="text" v-model="title">
        <div class="form-text">Por exemplo: Programador Javascript e VueJS.</div>
      </div>
    </div>
    <div class="row mt-3">
      <div class="col">
        <label class="form-label">Descrição</label>
        <textarea class="form-control" type="text" v-model="description"></textarea>
        <div class="form-text">Informe os detalhes da vaga.</div>
      </div>
    </div>
    <div class="row mt-3">
      <div class="col">
        <label class="form-label">Salário</label>
        <input class="form-control" type="number" v-model="salary">
        <div class="form-text">Informe o salário.</div>
      </div>
      <div class="col">
        <label class="form-label">Modalidade</label>
        <select class="form-select" v-model="model">
          <option value="" disabled>-- Selecione --</option>
          <option value="1">Home Office</option>
          <option value="2">Presencial</option>
        </select>
        <div class="form-text">Informe o modelo da vaga.</div>
      </div>
      <div class="col">
        <label class="form-label">Tipo</label>
        <select class="form-select" v-model="type">
          <option value="" disabled>-- Selecione --</option>
          <option value="1">CLT</option>
          <option value="2">PJ</option>
        </select>
        <div class="form-text">Informe o tipo de contratação.</div>
      </div>
    </div>
    <div class="row mt-3">
      <div class="col">
        <button type="submit" class="btn btn-primary" v-on:click="saveVacancy()">Cadastrar</button>
      </div>
    </div>
  </div>
</template>
  
<script>
  export default {
    name: 'PublishVacancy',
    data: () => ({
      title: '',
      description: '',
      salary: '',
      model: '',
      type: ''
    }),
    methods: {
      saveVacancy() {
        let vacancys = JSON.parse(localStorage.getItem('vacancys'))

        if (!vacancys) {
          vacancys = []
        }

        vacancys.push({
          title: this.title,
          description: this.description,
          salary: this.salary,
          model: this.model,
          type: this.type
        })

        localStorage.setItem('vacancys', JSON.stringify(vacancys))
      }
    }
  }
</script>
  
<style></style>