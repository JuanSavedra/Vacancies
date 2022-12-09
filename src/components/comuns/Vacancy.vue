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
      title: {
        type: String,
        required: true
      },
      description: {
        type: String, 
        default() {
          return "O contratante não adicionou uma descrição para esse curso"
        }
      },
      salary: {
        type: [String, Number], 
        required: true
      },
      model: {
        type: String, 
        required: true
      },
      type: {
        type: String, 
        required: true
      },
      publicationDate: {
        type: String, 
        required: true
      }
    },
    created() {

    }
  }
</script>