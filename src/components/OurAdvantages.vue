<template>
    <div class="container my-5">
        <div class="text-start">
            <!-- <p class="text-muted mb-1 text-uppercase">Features</p> -->
            <h2 class="display-5 text-uppercase" style="color: var(--bg-primary);">Our Advantages</h2>
        </div>
        <div class="row justify-content-center align-items-center">
            <div class="col-md-6">
                <p class="text-start fs-5 mb-4">
                    Zeil after having made its mark in the industrial Lubricants Sector is looking at establishing a
                    strong
                    footprint in the Automotive Sector with the launch of its Motor Oils.
                </p>
                <div class="row g-1">
                    <div class="col-md-6" v-for="(advantage, index) in advantages" :key="index">
                        <div class="d-flex align-items-center">
                            <i class="me-3 fs-4" :class="advantage.icon"></i>
                            <span>{{ advantage.text }}</span>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-md-6">
                <img src="/img/engine.png" alt="Engine" class="img-fluid" />
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'OurAdvantages',
    data() {
        return {
            advantages: [
                { icon: 'bi bi-shield-check', text: 'Protect Engine Wear & Tear' },
                { icon: 'bi-gear-wide-connected', text: 'Unique Friction Control Formula' },
                { icon: 'bi-cloud-minus', text: 'Minimize Engine Carbon deposits' },
                { icon: 'bi-lightning-charge', text: 'It Ensures Maximum power' }
            ]
        }
    }
}
</script>

<style scoped></style>