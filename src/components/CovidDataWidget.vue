<template>
  <div class="widget">
    <div class="card">
      <h3>Total Cases</h3>
      <p class="cases">
        {{ data.cases ? data.cases.toLocaleString() : "N/A" }}
      </p>
    </div>
    <div class="card">
      <h3>Total Deaths</h3>
      <p class="deaths">
        {{ data.deaths ? data.deaths.toLocaleString() : "N/A" }}
      </p>
    </div>
    <div class="card">
      <h3>Total Recovered</h3>
      <p class="recovered">
        {{ data.recovered ? data.recovered.toLocaleString() : "N/A" }}
      </p>
    </div>
    <div class="card">
      <h3>Active Cases</h3>
      <p class="active">
        {{ data.active ? data.active.toLocaleString() : "N/A" }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "CovidDataWidget",
  props: {
    data: {
      type: Object,
      required: true,
    },
  },
};
</script>
