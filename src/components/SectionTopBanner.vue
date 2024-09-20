<template>
    <div class="banner-container">
        <img src="/img/productBanner.jpg" alt="Product Banner" class="banner-image">
        <div class="overlay">
            <h1 class="banner-title">{{ pageName }}</h1>
        </div>
    </div>
</template>

<script>
export default { 
    data() {
        return {
            pageName: ''
        };
    },
    mounted() {
        let pageName = this.$route.path.split('/').pop();
        this.pageName = pageName.replace(/-/g, ' ');
    }, 
};
</script>

<style scoped>
.banner-container {
    position: relative;
    width: 100%;
    overflow: hidden;
}

.banner-image {
    width: 100%;
    height: 250px;
    object-fit: cover;
}

.overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(255, 0, 0, 0.6); 
    display: flex;
    justify-content: center;
    align-items: center;
}

.banner-title {
    font-size: 4rem;
    color: white;
    font-weight: bold;
    text-transform: uppercase;
    text-align: center;
    text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.5);
    /* Improved readability */
}
</style>