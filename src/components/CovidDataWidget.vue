<template>
  <div class="covid-widget">
    <div class="card" v-if="data">
      <h3>Total Cases</h3>
      <p>{{ data.cases ? data.cases.toLocaleString() : "N/A" }}</p>
    </div>
    <div class="card" v-if="data">
      <h3>Active Cases</h3>
      <p>{{ data.active ? data.active.toLocaleString() : "N/A" }}</p>
    </div>
    <div class="card" v-if="data">
      <h3>Recovered</h3>
      <p>{{ data.recovered ? data.recovered.toLocaleString() : "N/A" }}</p>
    </div>
    <div class="card" v-if="data">
      <h3>Deaths</h3>
      <p>{{ data.deaths ? data.deaths.toLocaleString() : "N/A" }}</p>
    </div>
    <div class="loading" v-if="loading">Loading...</div>
    <div class="error" v-if="error">{{ error }}</div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "CovidDataWidget",
  data() {
    return {
      data: null,
      loading: true,
      error: null,
    };
  },
  async created() {
    try {
      const response = await axios.get("https://disease.sh/v3/covid-19/all");
      this.data = response.data;
      this.loading = false;
    } catch (err) {
      this.error = "Error fetching data: " + err.message;
      this.loading = false;
    }
  },
};
</script>
