<template>
    <div>
      <div id="carouselExampleCaptions" class="carousel slide" data-bs-ride="carousel">
        <div class="carousel-indicators">
          <button
            v-for="(image, index) in images"
            :key="index"
            :data-bs-target="'#carouselExampleCaptions'"
            :data-bs-slide-to="index"
            :class="{ active: index === 0 }"
            :aria-current="index === 0 ? 'true' : false"
            :aria-label="'Slide ' + (index + 1)"
          ></button>
        </div>
        <div class="carousel-inner">
          <div
            v-for="(image, index) in images"
            :key="index"
            class="carousel-item"
            :class="{ active: index === 0 }"
            data-bs-interval="2000"
          >
            <img :src="image.src" class="d-block w-100" :alt="image.alt">
            <div class="carousel-caption d-none d-md-block">
              <h5>{{ image.label }}</h5>
              <p>{{ image.content }}</p>
            </div>
          </div>
        </div>
        <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide="prev">
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide="next">
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Next</span>
        </button>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        images: [
          {
            src: '/img/banner/1.jpg',
            alt: 'First slide',
            label: 'First slide label',
            content: 'Some representative placeholder content for the first slide.'
          },
          {
            src: '/img/banner/2.jpg',
            alt: 'Second slide',
            label: 'Second slide label',
            content: 'Some representative placeholder content for the second slide.'
          },
          {
            src: '/img/banner/3.jpg',
            alt: 'Third slide',
            label: 'Third slide label',
            content: 'Some representative placeholder content for the third slide.'
          }
        ]
      };
    }
  };
  </script>
  
  <style scoped>
  /* .carousel-item img {
    height: 400px;
    object-fit: cover;
  } */
  </style>
  