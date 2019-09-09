<template>
  <div class="container">
    <div class="row p-3">
      <div class="col col-6 p-2" v-for="item in companies" v-bind:key="item">
        <Companies :company="item" />
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import Companies from '~/components/Companies'

export default {
  components: {
    Companies
  },
  data () {
    return {
      companies: []
    }
  },
  mounted () {
    const self = this
    axios.get('http://localhost:8000/launches/getCompanies').then((res) => {
      self.companies = res.data.data
    })
  }
}
</script>
