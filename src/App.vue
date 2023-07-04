<script>
  import Chart from "./components/Chart.vue"

  export default {
    name: 'App',
    components: { Chart }
  }
</script>

<template>
  <header>
    <div id="logo-box">
      <img src="./assets/datafox.png" alt="datafox">
      <label>DATA<span>FOX</span></label>
    </div>
  </header>

  <main>
  <div id="chart-container">
    <div v-for="n in 10" class="chart-box">
      <div class="chart-name">Chart #{{ n }}</div>
      <Chart />
    </div>
  </div>
  </main>
</template>

<style scoped>

.chart-name {
  text-align: center;
  font-weight: 500;
}
.chart-box {
  height: 300px;
  border: 1px solid rgb(233, 233, 233);
  border-radius: 10px;
  padding: 10px;
  padding-bottom: 40px;
  margin-bottom: 20px;
  box-shadow: 4px 4px 8px 0px rgba(34, 60, 80, 0.2);
  display: flex;
  flex-direction: column;
}

#chart-container {
  display: flex;
  flex-direction: column;
  padding: 30px;
}

#logo-box {
  display: flex;
  align-items: center;
}

#logo-box img {
  width: 40px;
}

#logo-box label {
  font-weight: 800;
  margin-left: 8px;
}

header {
  padding: 20px 40px 20px 40px;
  display: flex;
  background-color: rgb(255, 234, 221);
  border-bottom: 1px solid rgb(255, 210, 182);
}

</style>