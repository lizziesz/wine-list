<template>
  <div class="container">
    <img src="wine.image" alt="wine image" />
    <img src="../assets/red-wine.jpg" alt="wine image" />
    {{ wine.name }}
  </div>
</template>

<script>
export default {
  name: 'Wine',

  props: {
    wine: {
      type: Object,
      required: true,
    },
  },
}
</script>

<style scoped>
.container {
  border: 1px solid darkgray;
}
</style>