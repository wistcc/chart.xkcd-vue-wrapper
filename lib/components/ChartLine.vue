<template>
  <svg />
</template>

<script>
import chartXkcd from 'chart.xkcd';

export default {
  name: 'ChartLine',
  props: {
    config: Object,
  },
  mounted: function() {
    new chartXkcd.Line(this.$el, this.config); 
  }
}
</script>
