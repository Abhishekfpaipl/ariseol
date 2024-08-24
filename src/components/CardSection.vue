<template>
    <div class="container mt-4">
        <div class="row row-cols-1 row-cols-md-4 g-4">
            <div v-for="(item, index) in items" :key="index" class="col">
                <div class="card h-100 border rounded-0" v-observe>
                    <div class="card-body d-flex align-items-center">
                        <i :class="item.icon" :style="{ color: item.color }"></i>
                        <span class="ms-3 fw-bold">{{ item.text }}</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            items: [
                { icon: 'bi bi-eye', color: '#FFA500', text: 'Lorem Ipsum' },
                { icon: 'bi bi-infinity', color: '#4169E1', text: 'Dolor Sitema' },
                { icon: 'bi bi-mortarboard', color: '#FF1493', text: 'Sed perspiciatis' },
                { icon: 'bi bi-hexagon', color: '#FF00FF', text: 'Magni Dolores' },
                { icon: 'bi bi-shuffle', color: '#87CEEB', text: 'Nemo Enim' },
                { icon: 'bi bi-star', color: '#FFA07A', text: 'Eiusmod Tempor' },
                { icon: 'bi bi-diamond', color: '#00CED1', text: 'Midela Teren' },
                { icon: 'bi bi-camera-video', color: '#4169E1', text: 'Pira Neve' },
                { icon: 'bi bi-diagram-3', color: '#DAA520', text: 'Dirada Pack' },
                { icon: 'bi bi-x-circle', color: '#DC143C', text: 'Moton Ideal' },
                { icon: 'bi bi-activity', color: '#FF4500', text: 'Verdo Park' },
                { icon: 'bi bi-brightness-high', color: '#32CD32', text: 'Flavor Nivelanda' }
            ]
        };
    }
};
</script>

<style scoped>
.card-body i {
    font-size: 1.5rem;
}

.before-enter {
    opacity: 0;
    transform: translateX(80px);
    transition: opacity 1.5s ease-out, transform 1.5s ease-out;
}

.enter {
    opacity: 1;
    transform: translateX(0);
}
</style>