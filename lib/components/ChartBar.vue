<template>
  <svg />
</template>

<script>
import chartXkcd from 'chart.xkcd';

export default {
  name: 'ChartBar',
  props: {
    config: Object,
  },
  mounted: function() {
    new chartXkcd.Bar(this.$el, this.config); 
  }
}
</script>
