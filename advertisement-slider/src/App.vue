<script>
  import Slider from './components/Slider.vue'


  export default{
    components: {
        Slider,
    },
    data() {
      return {
        slides: [
          {
            title: 'Coca-Cola - Open Happiness',
            text: 'Experience the refreshing taste of Coca-Cola and open happiness with every sip.'
          },
          {
            title: 'Coca-Cola - Taste the Feeling',
            text: 'Taste the feeling of happiness and joy with Coca-Cola.'
          },
          {
            title: 'Coca-Cola - Always Coca-Cola',
            text: 'Enjoy every moment of your life with the delicious taste of Coca-Cola.'
          },
        ],
      };
    },
  };
</script>

<template>
  <div id="app">
    <slider :slides="slides" />
  </div>
</template>

<style scoped>
 
</style>
