<template>
  <svg>
    <circle v-for="(item, index) in dataset"
            :key="index"
            :cx="item[0]"
            :cy="item[1]"
            r="10"
            fill='#fff' />
  </svg>
</template>

<script>
import dataset from './dataset'

export default {
  data() {
    return {
      dataset
    }
  }
}
</script>

<style>

</style>
