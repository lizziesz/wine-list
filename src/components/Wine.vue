<template>
  <div class="container">
    <!-- <img src="wine.image" alt="wine image" /> -->
    <img :src="image" alt="wine image" class="image" />
    <div class="details">
      <h3>{{ wine.name }}</h3>
      <p>{{ wine.region }}</p>
      <p>{{ wine.variety }}</p>
      <p>${{ wine.price }}</p>
    </div>
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

  computed: {
    image() {
      return this.wine.type === 'red' ? '/img/red-wine.jpg' : '/img/white-wine.jpg';
    }
  },
}
</script>

<style scoped>
.container {
  border: 1px solid darkgray;
  display: flex;
  flex-direction: column;
  height: 100%;
  margin: 10px;
}

.image {
  max-width: 100%;
  object-fit: contain;
}

.details {
  flex: 1;
}

.details h3 {
  padding: 5px;
}
</style>