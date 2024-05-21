<template>
  <div class="q-pa-md">
    <q-carousel
      swipeable
      animated
      v-model="slide"
      thumbnails
      infinite
    >
      <q-carousel-slide class="carousel-slide" :name="1" :img-src="images.mountains" />
      <q-carousel-slide class="carousel-slide" :name="2" :img-src="images.parallax1" />
      <q-carousel-slide class="carousel-slide" :name="3" :img-src="images.parallax2" />
      <q-carousel-slide class="carousel-slide" :name="4" :img-src="images.quasar" />
    </q-carousel>
  </div>
</template>

<script>
import { ref } from 'vue'
import mountains from '../assets/emel_LE_auto_x2.jpg'
import parallax1 from '../assets/pabji_LE_auto_x2.jpg'
import parallax2 from '../assets/gensin_LE_auto_x2.jpg'
import quasar from '../assets/epep.jpeg'

export default {
  setup () {
    const images = {
      mountains,
      parallax1,
      parallax2,
      quasar
    }
    return {
      slide: ref(1),
      images
    }
  }
}
</script>

<style scoped>
.carousel-slide {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%; 
}

.carousel-slide img {
  width: 8%; 
  height: auto; 
  object-fit: cover; 
}
</style>
