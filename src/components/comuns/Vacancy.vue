<template>
  <div class="card">
    <div class="card-header bg-dark text-white">{{title}}</div>
    <div class="card-body">
      <p>{{description}}</p>
    </div>
    <div class="card-footer">
      <small class="text-muted">
        Salário: R${{salary}} | Modalidade: {{model}} | Tipo: {{type}} | Publicação: {{publicationDate}}
      </small>
    </div>
  </div>
</template>

<script>
  export default {
    name: "Vacancy",
    props: {
      title: String,
      description: String,
      salary: [Number, String],
      model: String,
      type: String,
      publicationDate: String
    },
    created() {

    }
  }
</script>