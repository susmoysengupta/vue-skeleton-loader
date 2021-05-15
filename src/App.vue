<template>
  <suspense>
      <template #default>
          <ProfileCard></ProfileCard>
      </template>
      <template #fallback>
          Loading...
      </template>
  </suspense>
</template>

<script setup>
import ProfileCard from './components/ProfileCard.vue'

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
