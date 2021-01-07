<template>
    <ChartDoughnutBase :chart-data="chartData"/>
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
            backgroundColor: ["#5283ff"],
            hoverBackgroundColor: ["#5283ff"],
            data: [90, 10],      
            percent: 68,       
            display: false     
          }
        ],
        options: {
          scaleShowLabels: false,
          
          showTooltips: true
        }
      };
    }
  }
};
</script>