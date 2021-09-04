<template>
  <header>Wine!</header>
  <WineList />
</template>

<script>
import WineList from './WineList';

export default {
  name: 'HomePage',

  components: {
    WineList
  }
}
</script>
