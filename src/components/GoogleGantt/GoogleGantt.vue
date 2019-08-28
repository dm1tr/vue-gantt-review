<template>
  <div>
      <GChart
        :settings="{ packages: ['gantt'] }"
        type="Gantt"
        :data="chartData"
        :options="chartOptions"
        ref="gChart"
      />
  </div>
</template>

<script>
import { GChart } from 'vue-google-charts';
import tasks from '../../data/gantt_tasks.js';
import chartOptions from './options.js';

export default {
  components: {
    GChart
  },
  methods: {
    mapTasks (tasks) {
      return tasks.map(task => {
        let dependencies = task.dependencies ? task.dependencies.join(',') : null
        return [
          task.id, 
          task.description, 
          new Date(Date.parse(task.start)), 
          new Date(Date.parse(task.end)), 
          null, 
          task.progress,
          dependencies
        ]
      })
    },
  },

  data () {
    return {
      chartData: [
        [
          { type: "string", label: "Task ID" },
          { type: "string", label: "Task Name" },
          { type: "date", label: "Start Date" },
          { type: "date", label: "End Date" },
          { type: "number", label: "Duration" },
          { type: "number", label: "Percent Complete" },
          { type: "string", label: "Dependencies" }
        ],
      ],
      chartOptions
    }
  },

  created () {
    this.chartData.push(...this.mapTasks(tasks))
  }
}
</script>

<style>

</style>