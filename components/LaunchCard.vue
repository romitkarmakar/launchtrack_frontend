<template>
  <div class="card">
    <div class="card-header">
      {{ launch.name }}
    </div>
  <div class="card-body">
    {{ launch.detail }}
  </div>
  <div class="card-footer">
    {{ launch.date }}
  </div>
  </div>
</template>

<script>
export default {
  props: {
    launch: Object
  }
}
</script>
