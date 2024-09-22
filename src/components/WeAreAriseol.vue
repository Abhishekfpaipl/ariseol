<template>
    <div class="container my-5">
        <div class="text-start mb-5">
            <!-- <p class="text-muted mb-1 text-uppercase">Features</p> -->
            <h2 class="display-5 text-uppercase" style="color: var(--bg-primary);">we are ariseol</h2>
        </div>
        <p class="text-center mb-5">Recognized worldwide as 'The specialist in synthetic lubricants', Ariseol is German
            company Specialized in the manufacturing and marketing of performance products. For more than 150 years,
            Airseol has been synonymous with: </p>
        <div class="row g-2">
            <div class="col" v-for="(card, index) in cards" :key="index">
                <div class="card rounded-0 h-100 p-3" style="background-color: var(--bg-primary);">
                    <i :class="card.icon" class="fs-1 primary-text"></i>
                    <p class="text-center fs-5 fw-bold">{{ card.title }}</p>
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
                { icon: 'bi bi-star-fill', title: 'Quality' },
                { icon: 'bi bi-lightbulb-fill', title: 'Innovation' },
                { icon: 'bi bi-flag-fill', title: 'Racing' }
            ]
        }
    }
}
</script>
<style lang="">

</style>