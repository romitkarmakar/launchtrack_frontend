<template>
  <div class="container">
    <div class="row p-3">
      <div v-for="item in companies" :key="item" class="col col-4 p-3">
        <nuxt-link :to="'/launches/'+ item.name">
          <Companies :company="item" />
        </nuxt-link>
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
