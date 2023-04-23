<template>
    <div class="slide" :class="{ active: active}">
        <h2 class="slide-title" v-html="formattedTitle"></h2>
        <p class="slide-text">{{ text }}</p>
    </div>
</template>

<script>
export default {
    props: {
        title: {
            type: String,
            required: true,
        },
        text: {
            type: String,
            required: true,
        },
        active:{
            type: Boolean,
            required: true,
        },
    },
    computed: {
        formattedTitle() {
            return this.title.replace(
                /Coca-Cola/g,
                '<span style="color:#D10000">Coca-Cola</span>'
            );
        }
    }
};

</script>

<style scoped>
.slide{
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    opacity: 0;
    transition: opacity 0.5s ease-in-out;
}

.slide.active {
    opacity: 1;
}
.slide-title {
  font-size: 32px;
  font-weight: bold;
  text-align: center;
  margin-bottom: 20px;
  color: #333
}

.slide-text {
  font-size: 25px;
  line-height: 1.5;
  text-align: center;
  color: #555;
}



</style>