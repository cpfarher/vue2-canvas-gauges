<template>
  <canvas class="canvas-gauges"></canvas>
</template>

<script>
import { LinearGauge } from 'canvas-gauges'

export default {

  props: {
    value: Number,
    options: {
      type: Object,
      default: () => ({})
    }
  },

  data: function () {
    return {
      chart: null
    }
  },

  mounted: function () {
    this.chart = new LinearGauge(Object.assign({}, this.options, {renderTo: this.$el, value: this.value}))
      .draw()
  },

  beforeDestroy: function () {
    this.chart.destroy()
  },

  watch: {
    value: function (val) {
      this.chart.value = val
    },
    options: function (opt) {
      this.chart.destroy()
      this.chart = new LinearGauge(Object.assign({}, this.options, {renderTo: this.$el, value: this.value})).draw()
    }
  }

}
</script>
