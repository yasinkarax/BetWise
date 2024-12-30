<template>
  <div class="p-4">
    <h2 class="text-xl mb-4">Upcoming Matches</h2>
    <ul>
      <li v-for="match in matches" :key="match.id" class="mb-4 p-4 border rounded-lg">
        <div class="flex justify-between">
          <span>{{ match.team1 }} vs {{ match.team2 }}</span>
          <span>{{ match.date }} - {{ match.time }}</span>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'UpcomingMatches',
  props: {
    matches: {
      type: Array,
      required: true
    }
  }
}
</script>

<style scoped>
/* Add your styles here */
</style>
