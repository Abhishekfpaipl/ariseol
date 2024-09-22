<template>
    <div class="container">
        <div class="text-start mb-5">
            <p class="text-muted mb-1 text-uppercase">Check</p>
            <h2 class="display-5 text-uppercase" style="color: var(--bg-primary);">Ariseol motor oil</h2>
        </div>
        <div class="sticky-nav my-4">
            <div class="d-flex justify-content-center align-items-center p-3 py-2 overflow-x-scroll" id="scroll"
                style="background-color:rgba(255, 206, 86, 0.2); border:1px solid rgba(255, 206, 86, 1) !important;">
                <div v-for="(section, index) in sections" :key="index">
                    <a :href="'#' + section.id" class="nav-link text-dark" @click.prevent="scrollToSection(section.id)"
                        :class="{ active: activeSection === section.id }">
                        {{ section.name }}
                    </a>
                </div>
            </div>
        </div>

        <div class="container">
            <section v-for="(section, index) in sections" :key="index" :id="section.id" class="section"
                style="padding-top:30px">
                <h3 class="p-2 text-center my-4 cutout">
                    <span>{{ section.name }}</span>
                </h3>
                <component :is="section.component" :product="subproduct" v-observe></component>
            </section>
        </div>
    </div>
</template>
<script>
import ProductTableSection from "@/components/ProductTableSection.vue"
import IsoSection from "@/components/IsoSection.vue"
import ProductBenefitSection from "@/components/ProductBenefitSection.vue"
import FacilitiesSection from "@/components/FacilitiesSection.vue"
export default {
    components: {
        ProductTableSection,
        IsoSection,
        ProductBenefitSection,
        FacilitiesSection,
    },
    data() {
        return {
            sections: [
                { id: 'Reports', name: 'Reports', component: 'ProductTableSection' },
                { id: 'ISO', name: 'ISO', component: 'IsoSection' },
                { id: 'Benefits', name: 'Benefits', component: 'ProductBenefitSection' },
                { id: 'Facilities', name: 'Facilities', component: 'FacilitiesSection' },
            ],
        }
    },
}
</script>
<style lang="">

</style>