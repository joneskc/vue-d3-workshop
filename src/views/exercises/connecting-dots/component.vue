<template>
  <svg>
    <path fill="none"
          stroke="yellow"
          stroke-width="5"
          :d="d" />
    <circle r="10"
            v-for="(item, index) in dataset"
            :cx="item[0]"
            :cy="item[1]"
            :key="index"
            fill="#fff"
            @click="onClick(item)" />
  </svg>
</template>

<script>
import * as d3 from 'd3'
import dataset from './dataset'

export default {
  data() {
    return {
      dataset
    }
  },
  methods: {
    onClick(item) {
      console.log('this is the item!', item)
    }
  },
  computed: {
    lineGenerator() {
      return d3.line()
      .x(v => v[0])
      .y(v => v[1])
    },
    d() {
      return this.lineGenerator(this.dataset)
    }
  }
}
</script>