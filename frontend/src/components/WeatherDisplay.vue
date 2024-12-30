<template>
  <div class="flex items-center p-4 border rounded-lg">
    <img :src="icon" alt="Weather Icon" class="w-12 h-12 mr-4">
    <div>
      <div class="text-xl">{{ temperature }}°C</div>
      <div class="text-sm text-gray-600">{{ condition }}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'WeatherDisplay',
  props: {
    icon: {
      type: String,
      required: true
    },
    temperature: {
      type: Number,
      required: true
    },
    condition: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>
/* Add your styles here */
</style>
