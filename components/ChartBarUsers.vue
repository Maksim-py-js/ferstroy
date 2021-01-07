<template>
    <ChartDoughnutBase :chart-data="chartData" />
</template>

<script>
import ChartDoughnutBase from "@/components/ChartDoughnutBase";

export default {
  components: {
    ChartDoughnutBase
  },
  data() {
    return {
      chartData: null
    };
  },
  mounted() {
    this.fillData();
  },
  methods: {
    fillData() {
      this.chartData = {
        label: {
          display: false,
        },
        datasets: [
          {
            backgroundColor: ["#db3e32"],
            hoverBackgroundColor: ["#db3e32"],
            data: [75, 25],             
            display: false     
          }
        ],
        options: {
          scaleShowLabels: false
      }
      };
    }
  }
};
</script>