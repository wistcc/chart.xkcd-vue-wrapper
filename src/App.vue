<template>
  <div id="app">
    <ChartLine :config="line" />
    <ChartBar :config="bar" />
    <ChartPie :config="pie" />
  </div>
</template>

<script>
import { ChartLine,  ChartBar, ChartPie } from '../lib';

export default {
  name: 'App',
  components: {
    ChartLine,
    ChartBar,
    ChartPie,
  },
  data: function() {
    return {
      line: {
        title: 'Bugs to fix in a sprint',
        xLabel: 'Day',
        yLabel: 'Bugs',
        data: {
          labels:['1', '2', '3', '4', '5', '6','7'],
          datasets: [{
            label: 'Plan',
            data: [1, 2, 3, 4, 5, 6 ,7],
          }, {
            label: 'Reality',
            data: [0, 0, 0, 0, 0, 0, 7],
          }]
        },
      },
      bar: {
        title: 'Bugs your coworker fixes vs you',
        data: {
          labels:['your coworker', 'you'],
          datasets: [{
            data: [100, 2],
          }]
        },
      },
      pie: {
        title: 'Bugs you create vs your whole team',
        data: {
          labels:[ 'you', 'your team'],
          datasets: [{
            data: [100, 2],
          }]
        }
      }, 
    };
  },
}
</script>
