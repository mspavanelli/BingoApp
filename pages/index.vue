<template>
  <div class="container">
    <BingoCard />
  </div>
</template>

<script>
import BingoCard from '~/components/BingoCard.vue'

export default {
  name: 'IndexPage',
  components: { BingoCard },
}
</script>

<style>
.container {
  @apply w-full h-screen bg-slate-100 flex items-center justify-center;
}
</style>
