<template>
     <div id="app">
        <Card
        v-for="(rocket, index) in rockets"
      :key="index"
      :imageUrl="rocket.flickr_images[0]"
      :title="rocket.name"
      :description="rocket.description"
    />
    </div>
  
</template>

<script>
import Card from './components/Card.vue';

export default {
  components: {
    Card,
  },
  data() {
    return {
      rockets: [],
    };
  },
  mounted() {

    this.fetchRocketData();
  },
  methods: {
    async fetchRocketData() {
      try {
        const response = await fetch('https://api.spacexdata.com/v4/rockets');
        const data = await response.json();
        this.rockets = data;
      } catch (error) {
        console.error('Error fetching rocket data:', error);
      }
    },
  },
};
</script>

