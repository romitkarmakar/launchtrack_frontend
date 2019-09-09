<template>
  <div class="card">
    <div class="card-header">{{ company.name }}</div>
    <div class="card-body justify-content-center">
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
