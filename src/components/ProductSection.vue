<template>
    <div class="container">
        <div class="text-start mb-5">
            <p class="text-muted mb-1 text-uppercase">Products</p>
            <h2 class="display-5 text-primary text-uppercase">Check Our Products</h2>
        </div>
        <div class="row">
            <div v-for="(product, index) in products" :key="index" class="col-md-4 mb-4" v-observe>
                <!-- <div class="card product-card h-100" @mouseenter="expandCard(index)" @mouseleave="collapseCard(index)"> -->
                <div class="card product-card h-100">
                    <img :src="product.image" class="img-fluid" :alt="product.title">
                    <div class="card-body d-flex flex-column">
                        <div class="icon-wrapper mb-2">
                            <i class="bi bi-gear-fill text-warning"></i>
                        </div>
                        <h5 class="card-title">{{ product.title }}</h5>
                        <!-- <p v-if="product.expanded" class="card-text mt-2">{{ product.description }}</p> -->
                        <p class="card-text mt-2">{{ product.description }}</p>
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
            products: [
                {
                    title: 'Greases',
                    image: 'https://clgoilindia.com/demo/assets/images/service/Grease-01.jpg',
                    description: 'We are engaged in offering a wide range of good Quality to our clients.',
                    expanded: false
                },
                {
                    title: 'Automotive Lubricants',
                    image: 'https://clgoilindia.com/demo/assets/images/service/Grease-02.jpg',
                    description: 'High-quality lubricants for all types of vehicles.',
                    expanded: false
                },
                {
                    title: 'Industrial Lubricants',
                    image: 'https://clgoilindia.com/demo/assets/images/service/Grease-03.jpg',
                    description: 'Specialized lubricants for industrial machinery and equipment.',
                    expanded: false
                }
            ]
        }
    },
    methods: {
        expandCard(index) {
            this.products[index].expanded = true;
        },
        collapseCard(index) {
            this.products[index].expanded = false;
        }
    }
}
</script>

<style scoped>
.product-card {
    transition: all 0.3s ease;
    overflow: hidden;
}

.product-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
}

.before-enter {
    opacity: 0;
    transform: translateY(80px);
    transition: opacity 1.5s ease-out, transform 1.5s ease-out;
}

.enter {
    opacity: 1;
    transform: translateY(0);
}
</style>