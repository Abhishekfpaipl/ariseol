<template>
    <div class="container my-5">
        <div class="row row-cols-1 row-cols-md-2 row-cols-lg-3 g-2">
            <div class="col"  v-for="(item, index) in items" :key="index">
                <div class="row align-items-center mb-3 p-3">
                    <div class="col-12">
                        <i class="bi text-warning display-1" :class="item.icon"></i>
                    </div>
                    <div class="col-12">
                        <span class="fs-1">{{ item.title }}</span>
                    </div>
                    <div class="col-12">
                        <p class="small">{{ item.text }}
                        </p>
                    </div>
                </div>

            </div>
        </div>

    </div>
</template>

<script>
export default {
    name: "AboutKeyFeatures",
    data() {
        return {
            items: [
                {
                    icon: "bi-bullseye",
                    title: "Our Mission",
                    text: "Our mission is to lead globally in providing customized greases and lubricants, delivering superior quality and innovative solutions tailored to meet the diverse needs of industries worldwide."
                },
                {
                    icon: "bi-eye",
                    title: "Our Vision",
                    text: "Our vision is to drive global expansion and innovation, addressing critical challenges while empowering our customers to succeed through the unmatched value of our products and services."
                },
                {
                    icon: "bi-gem",
                    title: "Our Values",
                    text: "Our values emphasize excellence, integrity, and sustainability, delivering top-quality solutions while honoring our commitment to eco-friendly practices and environmental stewardship."
                }
            ]
        };
    },
};
</script>