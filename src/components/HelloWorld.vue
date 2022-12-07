<script setup>
defineProps({
  msg: {
    type: String,
    required: true
  }
})
</script>

<template>
  <div class="">
    <h1 class="text-amber-600 ani">{{ msg }}</h1>
  </div>
</template>

<style scoped>
.ani {
  text-shadow: -1px -1px 0 #000, 1px -1px 0 #000, -1px 1px 0 #000, 1px 1px 0 #000;
  animation: 2s pulsate infinite;
}

@keyframes pulsate {
  50% {
    stroke-width: 5px
  }
}
</style>

