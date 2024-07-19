<template>
  <button :class="isSelected ? 'selected' : ''" @click="toggle">
    {{ number }}
  </button>
</template>

<script>
export default {
  name: 'BingoNumber',
  props: {
    number: {
      type: [Number, String],
      required: true,
    },
  },
  data() {
    return {
      isSelected: false,
    }
  },
  methods: {
    toggle() {
      this.isSelected = !this.isSelected
    },
  },
}
</script>

<style>
button {
  @apply bg-slate-300 text-slate-600 h-16 shadow rounded text-xl transition-all;
}

.selected {
  @apply bg-emerald-500 text-emerald-900;
}
</style>
