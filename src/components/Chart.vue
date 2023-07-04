<script>
    import { Bar } from 'vue-chartjs'
    import { Chart as ChartJS, Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale } from 'chart.js'

    ChartJS.register(Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale)

    export default {
        name: 'BarChart',
        components: { Bar },
        data() {
            return {
                chartData: {
                    labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange', 'Orange', 'Orange' ,'Orange','Purple', 'Orange', 'Orange', 'Orange' ,'Orange','Purple', 'Orange', 'Orange', 'Orange' ,'Orange','Orange', 'Orange', 'Orange' ,'Orange','Orange', 'Orange', 'Orange' ,'Orange'],
                    datasets: [{
                        label: '# of Votes',
                        borderColor: '#36A2EB',
                        backgroundColor: '#9BD0F5',
                        data: [12, 19, 3, 5, 2, 3,12, 19, 3, 5, 2, 3,12, 19, 3, 5, 2, 3,12, 19, 3, 5, 2, 3, 3,12, 19, 3, 5, 2, 3,3,12, 19, 3, 5, 2, 3],
                        borderWidth: 1
                    }]
                },
                chartOptions: {
                    responsible: false,
                    maintainAspectRatio: false,
                }
            }
        }
    }
</script>

<template>
   <Bar
    :options="chartOptions"
    :data="chartData"
  />
</template>

<style>

</style>