<template>
  <div class="card">
    <div class="card-header">
      {{ company.name }}
    </div>
    <div class="card-body justify-content-center">
      <img :src="company.image" height="150" width="250" class="mx-auto d-block">
    </div>
  </div>
</template>
<script>
export default {
  props: {
    company: Object
  }
}
</script>

<style>
  .card{
    background-color:whitesmoke;
    height: 100%;
    width: 90%;
  }
</style>
