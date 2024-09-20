<template>
    <div class="container">
        <div class="row">
            <h1 class="px-2 text-center mb-5">Why Choose Us?</h1> 
            <div class="col-md-6 position-relative">
                <img src="/img/whychooseus.jpeg" alt="Why choose us" class="img-fluid w-100">
            </div>
            <div class="col-md-6  text-start">
                <div class="accordion" id="accordionExample">
                    <div class="accordion-item rounded-0" v-for="(item, index) in accordionData" :key="index">
                        <h2 class="accordion-header">
                            <button class="accordion-button fw-bold text-dark" type="button" data-bs-toggle="collapse"
                                :data-bs-target="'#collapseOne' + index" aria-expanded="true"
                                :aria-controls="'collapseOne' + index">
                                {{ item.title }}
                            </button>
                        </h2>
                        <div :id="'collapseOne' + index" class="accordion-collapse collapse"
                            :class="{ show: index === 0 }" data-bs-parent="#accordionExample">
                            <div class="accordion-body text-start">
                                {{ item.content }}
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

</template>

<script>
export default {
    name: 'WhyUsComponent',
    data() {
        return {
            accordionData: [
                {
                    title: "Atmospheric Style Soap Manufacturing Vessels (Kettles)",
                    content: "These vessels are designed for the efficient production of soap-based greases. They operate under atmospheric pressure, ensuring controlled reactions and consistent product quality.",
                },
                {
                    title: "20 MT/day Grease Production Facilities",
                    content: "Our facilities are equipped to produce up to 20 metric tons of grease per day. This ensures high capacity and meeting large-scale production demands.",
                },
                {
                    title: "25 KL/day Lube Blending Facilities",
                    content: "We offer lube blending capabilities of 25 kiloliters per day. This facilitates the precise mixing of lubricants to achieve the desired formulations and quality.",
                },
                {
                    title: "High-Speed Shear for Non-Soap Thickened Greases",
                    content: "Our high-speed shear facilities are particularly effective for processing non-soap thickened greases. This enhances the consistency and performance of these specialized products.",
                },
                {
                    title: "High-Pressure Milling",
                    content: "This process ensures the fine grinding and uniform dispersion of grease components. This results in improved texture and performance.",
                },
                {
                    title: "Grease De-Aeration",
                    content: "Our de-aeration systems remove trapped air from greases. This helps in achieving a smooth, bubble-free product and enhances its stability and performance.",
                },
                {
                    title: "Oil Blending Facilities",
                    content: "We provide advanced oil blending capabilities to ensure the precise formulation of lubricants and greases. This optimizes their effectiveness and compatibility.",
                },
                {
                    title: "Steam and Thermal Oil Heating",
                    content: "Our heating systems utilize steam and thermal oil to maintain optimal temperatures during production. This ensures consistent quality and efficiency.",
                },
                {
                    title: "Bulk Storage Facilities",
                    content: "Our bulk storage solutions are designed to safely and efficiently handle large quantities of raw materials and finished products. This ensures easy access and inventory management.",
                },
                {
                    title: "Advanced Filling and Packing Machines",
                    content: "State-of-the-art filling and packing equipment ensure accurate, efficient, and hygienic packaging of greases and lubricants. This meets industry standards and customer requirements.",
                },
            ],
        };
    },
}
</script>
<style scoped>
.accordion-button:not(.collapsed) {
    color: #0d6efd;
    background-color: white;
}
</style>