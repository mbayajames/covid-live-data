<template>
  <header>
    <img src="/src/assets/logo.png" alt="Logo">
    <h1>COVID-19 Live Data</h1>
  </header>
  <main>
    <p v-if="error" class="error">{{ error }}</p>
    <p v-else-if="loading" class="loading">Loading data...</p>
    <CovidDataWidget v-else :data="covidData" />
  </main>
</template>

<script>
import CovidDataWidget from './components/CovidDataWidget.vue'
import axios from 'axios'

export default {
  name: 'App',
  components: {
    CovidDataWidget
  },
  data() {
    return {
      covidData: {},
      loading: true,
      error: null
    }
  },
  async created() {
    try {
      const response = await axios.get('https://disease.sh/v3/covid-19/all')
      this.covidData = response.data
      this.loading = false
    } catch (err) {
      this.error = 'Failed to fetch COVID-19 data. Please try again later.'
      this.loading = false
    }
  }
}
</script>