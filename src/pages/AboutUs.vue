<template>
    <div style="padding-top: 66px;">
        <SectionTopBanner />
        <div class="container bg-white rounded-top-5" style="margin-top: -40px;" v-observe>
            <SuccessStory :tests="tests" v-observe />
            <div class="my-5">
                <TeamInfoSection :techTeam="techTeam" :marketingTeam="marketingTeam" :managementTeam="managementTeam"
                    v-observe />
            </div>
        </div> 
        <div class="">
            <AutoScrolling :links="country" imageFilter="invert(1)" textColor="text-white" textSize="fs-4 pt-3"
                bgColor="#02539E" title="we are currently working in" v-observe />
        </div>
        <div class="container py-5 rounded-top-5 bg-white" style="margin-top: -40px;"> 
            <div class="">
                <WhyChooseUs v-observe />
            </div>
            <div class="">
                <AboutKeyFeatures v-observe />
            </div> 
        </div>
        <div class="my-5">
            <OurCoreValues />
        </div>

    </div>
</template>
<script>
import WhyChooseUs from "@/components/WhyChooseUs.vue";  

import SuccessStory from "@/components/SuccessStory.vue"; 
import TeamInfoSection from "@/components/TeamInfoSection.vue";  
import AutoScrolling from "@/components/AutoScrolling.vue";
import OurCoreValues from "@/components/OurCoreValues.vue";
import AboutKeyFeatures from "@/components/AboutKeyFeatures.vue";
import SectionTopBanner from "@/components/SectionTopBanner.vue";
export default {
    name: "AboutUs",
    components: {
        WhyChooseUs,  
        AutoScrolling,
        OurCoreValues,
        SuccessStory,
        TeamInfoSection,
        AboutKeyFeatures,
        SectionTopBanner,
    },
    data() {
        return {
            customFields: [
                {
                    name: "Shop Name",
                    value: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Ab soluta quis nihil adipisci voluptate impedit placeat aperiam doloremque quasi voluptatibus ."
                },
                {
                    name: "Description",
                    value: " Lorem ipsum dolor sit amet consectetur adipisicing elit. Ab soluta quis nihil adipisci voluptate impedit placeat aperiam doloremque quasi voluptatibus."
                },
                {
                    name: "Description",
                    value: " Lorem ipsum dolor sit amet consectetur adipisicing elit. Ab soluta quis nihil adipisci voluptate impedit placeat aperiam doloremque quasi voluptatibus."
                },
                {
                    name: "Description",
                    value: " Lorem ipsum dolor sit amet consectetur adipisicing elit. Ab soluta quis nihil adipisci voluptate impedit placeat aperiam doloremque quasi voluptatibus."
                },
                {
                    name: "Description",
                    value: " Lorem ipsum dolor sit amet consectetur adipisicing elit. Ab soluta quis nihil adipisci voluptate impedit placeat aperiam doloremque quasi voluptatibus."
                },
            ],
            links: [
                {
                    id: 1,
                    img: 'img/users/1.png',
                    title: "Member 1",
                    description: "Tailored designs to fit your unique brand identity.",
                },
                {
                    id: 2,
                    img: 'img/users/2.png',
                    title: "Member 2",
                    description: "Optimized for seamless experiences on all devices.",
                },
                {
                    id: 3,
                    img: 'img/users/3.png',
                    title: "Member 3",
                    description: "Efficient CMS solutions for easy content updates.",
                },
                {
                    id: 4,
                    img: 'img/users/4.png',
                    title: "Member 4",
                    description: "Robust online stores to boost your sales.",
                },
                {
                    id: 5,
                    img: 'img/users/5.png',
                    title: "Member 5",
                    description: "Bespoke applications to meet your business needs.",
                },
            ],
        }
    },
    computed: {
        techTeam() {
            return this.$store.getters['about/getTechTeam']
        },
        marketingTeam() {
            return this.$store.getters['about/getMarketingTeam']
        },
        managementTeam() {
            return this.$store.getters['about/getManagementTeam']
        },
        country() {
            return this.$store.getters.getCountries
        },
        // pageTitle() {
        //     return this.$route.meta.pageTitle;  // Access the page title from the route meta field
        // }
    },
}
</script>