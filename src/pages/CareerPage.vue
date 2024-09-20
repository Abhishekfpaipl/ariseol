<template>
    <div style="padding-top: 66px;">
        <SectionTopBanner />
        <div class="container py-5 rounded-top-5 bg-white" style="margin-top: -40px;" v-observe>
            <div class="row">
                <div class="col-12 col-md-6 d-flex justify-content-center align-items-center">
                    <img src="/img/career-benefit.svg" style="width: 500px; max-width: 80%" alt="">
                </div>
                <div class="col-12 col-md-6 text-center mt-4 mt-md-0">
                    <h1>" We encourage new ideas and professionalism mixed with teamwork to achieve your
                        career goals as well as making the customer satisfied. "</h1>
                </div>

            </div>
        </div>
        <CareerSection />
        <div class="py-5" style="background-color: var(--bg-forth)">
            <div class="container">
                <h3 class="text-capitalize mb-4">Employee Benefits</h3>
                <div class="row row-cols-1 row-cols-md-3 row-cols-lg-4">
                    <div v-for="(data, index) in works" :key="index" class="col">
                        <div class="d-flex align-items-center border my-1 ps-5 ps-md-2">
                            <i :class="data.icon" class="fs-4 p-1"></i>
                            <small class="fw-bold text-capitalize ms-3">{{ data.heading }}</small>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class=" container py-5" v-observe>
            <h3 class="text-center ">Our Core Values</h3>
            <p class="text-center container">
                One thing that we've tried to keep consistent through all these years is our core set of values and
                beliefs.
                They have helped us get to where we are today, and they guide us as we grow. We inculcate these
                values
                in
                everything we do - from the littlest of things to the biggest of decisions.
            </p>
            <div class="p-2 row">
                <div v-for="(data, index) in datas" :key="index" class="col-12 col-md-6 g-3">
                    <div class="d-flex align-items-center border p-2">
                        <img :src="data.icon" :alt="data.name" style="width: 8%; filter: grayscale(1);" class="mx-3">
                        <div class=" ms-2">
                            <span class="fw-bold">{{ data.heading }}</span>
                            <p>{{ data.text }}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>

    </div>
</template>

<script>
import SectionTopBanner from "@/components/SectionTopBanner.vue"
import CareerSection from "@/components/CareerSection.vue";
export default {
    name: 'CareerPage',
    components: {
        SectionTopBanner,
        CareerSection
    },
    data() {
        return {
            datas: [
                {
                    icon: 'https://tss-static-images.gumlet.io/career-revamp/think different.svg',
                    heading: 'Think Different',
                    text: 'Random ideas, new suggestions, and challenging the norm are always welcome.'
                },
                {
                    icon: 'https://tss-static-images.gumlet.io/career-revamp/ownership of work.svg',
                    heading: 'Stay Weird, Be Yourself',
                    text: 'The Souled Store is strictly a judgment-free zone. Just be the best version of yourself.'
                },
                {
                    icon: 'https://tss-static-images.gumlet.io/career-revamp/respect everyone.svg',
                    heading: 'Respect Everyone',
                    text: 'Treat others how you’d like to be treated, and you have a happy family.'
                },
                {
                    icon: 'https://tss-static-images.gumlet.io/career-revamp/Growth and learning.svg',
                    heading: 'Ownership Of Work',
                    text: 'Give every task, small or big, your best shot. Always remember- 99% right is 100% wrong.'
                },
                {
                    icon: 'https://tss-static-images.gumlet.io/career-revamp/stay weird.svg',
                    heading: 'Take Initiative',
                    text: 'Want to change something? Change it. See something that needs fixing? Fix it.'
                },
                {
                    icon: 'https://tss-static-images.gumlet.io/career-revamp/take initiative.svg',
                    heading: 'Growth & Learning',
                    text: 'Work with various teams and departments and learn something new every day.'
                },
            ],
            works: [
                {
                    icon: 'bi bi-currency-rupee',
                    heading: 'Competitive Salary'
                },
                {
                    icon: 'bi bi-bounding-box',
                    heading: 'Open Office Culture'
                },
                {
                    icon: 'bi bi-graph-up-arrow',
                    heading: 'Fast Growing Startup'
                },
                {
                    icon: 'bi bi-people-fill',
                    heading: 'Equal Opportunities'
                },
                {
                    icon: 'bi bi-emoji-smile',
                    heading: 'Boosting Employee Morale'
                },
                {
                    icon: 'bi bi-heart',
                    heading: 'Improving Well-being'
                },
                {
                    icon: 'bi bi-lightning',
                    heading: 'Increasing Productivity'
                },
                {
                    icon: 'bi bi-check2-circle',
                    heading: 'Fulfilling Legal Requirements'
                }
            ],
            name: '',
            designation: '',
            note: ''
        }
    },
    methods: {
        submitQuery() {
            if (this.name != "" && this.designation != "" && this.note != "") {
                const phoneNumber = '918860012001'; // Replace with your WhatsApp number
                const message = `Hello, my name is ${this.name}. I am : ${this.designation}. Here are some additional notes: ${this.note}.`;
                const whatsappUrl = `https://api.whatsapp.com/send?phone=${phoneNumber}&text=${encodeURIComponent(message)}`;
                window.open(whatsappUrl, '_blank');
                this.name = "",
                    this.service = "",
                    this.note = "";
            }
        }
    },

}
</script>

<style lang="scss" scoped></style>