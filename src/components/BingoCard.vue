<template>
  <div class="card">
    <div class="table">
      <Number v-for="number in B" :key="number" :number="number" />
      <Number v-for="number in I" :key="number" :number="number" />
      <Number v-for="number in N" :key="number" :number="number" />
      <Number v-for="number in G" :key="number" :number="number" />
      <Number v-for="number in O" :key="number" :number="number" />
    </div>
  </div>
</template>

<script>
// import { mapGetters } from 'vuex'

import BingoNumber from '@/components/BingoNumber.vue'

export default {
  name: 'BingoCard',
  components: {
    Number: BingoNumber,
  },
  data() {
    return {
      B: [2, 4, 11, 1, 9],
      I: [16, 20, 28, 25, 27],
      N: [45, 38, 'Free', 33, 44],
      G: [49, 46, 48, 55, 47],
      O: [63, 75, 64, 72, 67],
    }
  },
}
</script>

<style>
.card {
  @apply w-11/12 rounded py-4;
}

.table {
  @apply grid grid-flow-col gap-2 grid-rows-[repeat(5,minmax(0,_1fr))] grid-cols-[repeat(5,minmax(0,_1fr))];
}
</style>
