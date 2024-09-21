<template>
  <div>
    <router-link to="/products" class="text-decoration-none text-dark">
      <img src="/img/banner/1.jpg" class="d-md-block d-none w-100"
        style="height: 600px;object-fit: cover;object-position: center;" alt="">
      <img src="/img/banner/1.jpg" class="d-md-none d-block w-100" alt="">
    </router-link>
  </div>
  <div class="container" style="margin-top: -50px;" v-observe>
    <div class="row">
      <div class="col-md-4 mb-4" v-for="(card, index) in cards" :key="index">
        <div class="card rounded-0 position-relative border-0">
          <div class="overlay"></div>
          <div class="d-flex justify-content-center align-items-center">
            <i v-if="card.icon" :class="card.icon" class="fs-1"></i>
          </div>
          <p class="card-title fs-1">{{ card.title }}</p>
          <p class="card-text">{{ card.description }}</p>
          <p class="smaller">Compared to conventional engine oil</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          title: '11%',
          description: "Torque",
          icon: 'bi bi-lightning-fill',
          backgroundImage: '/img/update.jpg',
        },
        {
          title: '22%',
          description: 'Performance Consistency',
          backgroundImage: '/img/grease.jpg',
          icon: 'bi bi-star-fill',
        },
        {
          title: '61%',
          description: "Protection",
          icon: 'bi bi-shield-fill',
          backgroundImage: '/img/industry.jpg',
        }
      ]
    };
  }
};
</script>

<style scoped>
.card {
  position: relative;
  overflow: hidden;
}

.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(255, 0, 0, 0.5);
  /* opacity: 1; */
}

.card-title,
.card-text {
  position: relative;
  /* Make sure text is above the overlay */
  z-index: 1;
}

.card:hover .card-img {
  transform: scale(1.05);
}
</style>
