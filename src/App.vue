<template>
  <div id="app">
    <Header />
      <Card
        v-for="(rocket, index) in rockets"
        :key="index"
        :imageUrl="rocket.flickr_images[0]"
        :title="rocket.name"
        :description="rocket.description"
      />
    <Footer />
  </div>
</template>


<script>
import Card from './components/Card.vue';
import Footer from './components/Footer.vue';
import Header from "./components/Header.vue";

export default {
  components: {
    Card,Footer, Header,
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

<style>
body {
  font-family: 'Arial', sans-serif;
  margin: 0;
  padding: 0;

}



</style>