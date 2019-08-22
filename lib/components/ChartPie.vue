<template>
  <svg />
</template>

<script>
import chartXkcd from 'chart.xkcd';

export default {
  name: 'ChartPie',
  props: {
    config: Object,
  },
  mounted: function() {
    new chartXkcd.Pie(this.$el, this.config); 
  }
}
</script>
