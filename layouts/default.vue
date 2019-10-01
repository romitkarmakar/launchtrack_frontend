<template><body class="sty">
  <div>
    <Navbar />
    <nuxt />
  </div>
          </body>
</template>

<script>
import Navbar from '~/components/Navbar'
export default {
  components: {
    Navbar
  }
}
</script>

<style>
  .sty{
    background-color: black
  }
</style>
