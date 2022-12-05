<template>
  <div>
    <h1>Home</h1>
  </div>
</template>
  
<script>
  export default {
    name: 'Home',
    activated() {
      console.log("Componente ativado.")
    },
    deactivated() {
      console.log("Componente desativado.")
    }
  }
</script>
  
<style></style>