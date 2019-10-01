<template>
  <div class="card" style="width:0px">
    <div class="card-header">{{ company.name }}</div>
    <div class="card-body justify-content-center" style="align:bottom">
      <img :src="company.image" height="100" class="mx-auto d-block" />
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
    width: 70%
  }
</style>

