

<template>
  <div class="slider">
    <div class="slides">
      <slide v-for="(slide, index) in slides" :key="index" :title="slide.title" :text="slide.text" :active="index === activeIndex" />
    </div>
    <div class="controls">
      <button v-for="(slide, index) in slides" :key="index" @click="setActiveIndex(index)" :class="{ active: index === activeIndex}"></button>
    </div>
  </div>
  
</template>


<script>
import Slide from './Slide.vue'

export default {
  components: {
    Slide,
  },
  props: {
    slides: {
      type: Array,
      required: true,
    },
  },
  data() {
    return {
      activeIndex: 0,
    };
  },
  methods: {
    setActiveIndex(index) {
      this.activeIndex = index;
    },
  },

};


</script>


<style scoped>
.slider {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.slides {
  width: 100%;
  height: 300px;
  position: relative;
  overflow: hidden;
}

.controls{
  display: flex;
  margin-top: 10px;
}

button {
  width: 20px;
  height: 15px;
  border-radius: 50%;
  margin-right: 10px;
  border: none;
  background-color: #ccc;
}

button.active{
  background-color: #333
}




</style>
