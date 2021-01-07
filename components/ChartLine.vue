<template>
    <div>
        <b-form-group class="d-flex">
            <b-form-radio
            v-for="(item, index) in btn"
            :key="index"
            v-model="radio"
            :name="item.label"
            :value="item.value"
            @change="updateChart"
            >
            {{ item.label }}
            </b-form-radio>
        </b-form-group>

        <ChartLineBase :chart-data="chartData"/>
    </div>

</template>

<style>
.bv-no-focus-ring {
  display: flex;
}
.custom-control {
  margin-right: 30px;
}
#line-chart {
  height: 300px !important;
}
</style>

<script>
import ChartLineBase from "@/components/ChartLineBase";

export default {
  components: {
    ChartLineBase
  },
  data() {
    return {
      btn: [
        { label: "Today", value: "day" },
        { label: "This Week", value: "week" }
      ],
      chartData: null,
      data: {
        day: [75172, 23179, 23477, 13772, 19774, 79528, 17312, 19673, 19948, 13694, 19139, 12777, 13310, 19477, 19773, 16747, 17454, 10973, 12874, 10320, 21489, 27459, 23977, 20807],
        week: [250400, 124378, 789045, 98445, 971513, 976340, 1279843]
      },
      labels: {
        day: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24],
        week: ["Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat"]
      },
      radio: "day"
    };
  },
  mounted() {
    this.fillData();
  },
  methods: {
    fillData() {
      this.chartData = {
        labels: this.labels[this.radio],
        datasets: [
          {
            borderColor: "#81894e",
            data: this.data[this.radio],
            label: "Profit"
          }
        ]
      };
    },
    updateChart() {
      this.$nextTick(() => {
        this.fillData();
      });
    }
  }
};
</script>