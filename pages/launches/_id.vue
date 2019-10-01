<template>
  <div class="container">
    <div class="row">
      <div v-for="item in launches" :key="item" class="col col-4 p-3">
        <LaunchCard :launch="item" />
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import LaunchCard from '~/components/LaunchCard'

export default {
  components: {
    LaunchCard
  },
  data () {
    return {
      id: this.$route.params.id,
      launches: []
    }
  },
  mounted () {
    const self = this
    axios.get(`http://localhost:8000/launches/get/${self.id}`).then((res) => {
      self.launches = res.data.data
    })
  }
}
</script>
