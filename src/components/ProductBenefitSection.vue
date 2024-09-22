<template>
    <div v-if="product.benefits" class="container mt-4 text-start"> 
        <div class="row border my-2" v-for="(benefit, index) in product.benefits" :key=index>
            <div class="col-12 d-flex align-items-center bg-light p-2 col-md-4">{{ benefit.title }}</div>
            <div class="col-12 d-flex align-items-center col-md-8 p-2">{{ benefit.content }}</div>
        </div>
    </div>
    <div v-else class="container mt-4 text-center">
        <h5>No benefits provided for this product.</h5>
    </div>
</template>

<script>
export default {
    name: 'ProductBenefitSection',
    props: {
        product: {
            type: Object,
            required: true,
        }
    },
}
</script>