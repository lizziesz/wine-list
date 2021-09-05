<template>
  <div class="list">
    <Wine
      v-for="wine in wines"
      :key="wine.name"
      :wine="wine"
    />
  </div>
</template>

<script>
import Wine from './Wine';
import wines from '../constants/wines.json';

export default {
  name: 'WineList',

  components: {
    Wine
  },

  data() {
    return {
      wines,
    };
  },
}
</script>

<style scoped>
.list {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  grid-gap: 1rem;
}
</style>