<template>
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2 row-col-lg-3 row-cols-xl-4 g-2">
      <div class="col" v-for="(image, index) in images" :key="index">
        <div class="card rounded-0 border-0 overflow-hidden">
          <img :src="image" alt="Gallery" class="w-100">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "GallerySection",
  data() {
    return {
      images: [
        "https://bootstrapmade.com/demo/templates/Bootslander/assets/img/gallery/gallery-1.jpg",
        "https://bootstrapmade.com/demo/templates/Bootslander/assets/img/gallery/gallery-2.jpg",
        "https://bootstrapmade.com/demo/templates/Bootslander/assets/img/gallery/gallery-3.jpg",
        "https://bootstrapmade.com/demo/templates/Bootslander/assets/img/gallery/gallery-4.jpg",
        "https://bootstrapmade.com/demo/templates/Bootslander/assets/img/gallery/gallery-5.jpg",
        "https://bootstrapmade.com/demo/templates/Bootslander/assets/img/gallery/gallery-6.jpg",
        "https://bootstrapmade.com/demo/templates/Bootslander/assets/img/gallery/gallery-7.jpg",
        "https://bootstrapmade.com/demo/templates/Bootslander/assets/img/gallery/gallery-8.jpg",
      ]
    }
  }
};
</script>

<style scoped>
.card:hover img {
  transform: scale(1.1);
  transition: transform 0.5s ease;

}
</style>
