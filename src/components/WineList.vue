<template>
  <div>
    Wines go here yo
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
  
  mounted() {
    console.log('wines', this.wines);
  }
}
</script>
