<template>
  <div id="app" class="min-h-screen flex flex-col">
    <header class="bg-blue-600 text-white p-4">
      <h1 class="text-2xl">Betwise</h1>
    </header>
    <main class="flex-grow p-4">
      <div class="container mx-auto">
        <h2 class="text-xl mb-4">Welcome to Betwise</h2>
        <p class="mb-4">Collect data about football matches, teams, players, and weather conditions to predict match results and goal counts.</p>
        <UpcomingMatches :matches="upcomingMatches" />
        <WeatherDisplay :icon="weather.icon" :temperature="weather.temperature" :condition="weather.condition" />
      </div>
    </main>
  </div>
</template>

<script>
import UpcomingMatches from './components/UpcomingMatches.vue'
import WeatherDisplay from './components/WeatherDisplay.vue'

export default {
  name: 'App',
  components: {
    UpcomingMatches,
    WeatherDisplay
  },
  data() {
    return {
      upcomingMatches: [
        { id: 1, team1: 'Team A', team2: 'Team B', date: '2023-10-01', time: '18:00' },
        { id: 2, team1: 'Team C', team2: 'Team D', date: '2023-10-02', time: '20:00' },
        // ...more matches
      ],
      weather: {
        icon: 'https://example.com/weather-icon.png',
        temperature: 22,
        condition: 'Sunny'
      }
    }
  }
}
</script>

<style>
/* Add your styles here */
</style>
