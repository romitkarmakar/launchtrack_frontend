<template>
  <div class="container">
    <div class="row">
      <div class="col col-6 p-3" v-for="item in launches" v-bind:key="item">
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
    console.log(this.$route.params.slug)
    const self = this
    axios.get(`http://localhost:8000/launches/get/${self.id}`).then((res) => {
      self.launches = res.data.data
    })
  }
}
</script>
