<template>
    <div class="container my-5">
        <div class="text-start mb-5">
            <p class="text-muted mb-1 text-uppercase">Ariseol</p>
            <h2 class="display-5 text-uppercase" style="color: var(--bg-primary);">Check Our Features</h2>
        </div>
        <div class="row g-3">
            <div v-for="(product, index) in products" :key="index" class="col-md-3 mb-4" v-observe>
                <div class="card h-100 rounded-0 shadow p-3 px-4" style="background-color: var(--bg-primary);">
                    <div class="rounded border border-dark bg-dark border-2 p-1"
                        style="width:60px; height:60px; margin-top:-40px;">
                        <i :class="product.icon" class="fs-1 text-warning"></i>
                    </div>
                    <p class="mt-3 text-capitalize text-start fw-bold text-white">{{ product.title }}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            products: [
                {
                    icon: 'bi bi-lightbulb',
                    title: 'Double easter technology',
                },
                {
                    icon: 'bi bi-people',
                    title: 'Centres of excellence',
                },
                {
                    icon: 'bi bi-infinity',
                    title: 'Creative and innovative lab',
                },
                {
                    icon: 'bi bi-gear',
                    title: 'Original equipment manufacturer',
                }
            ]

        }
    },
}
</script>