<template>
    <div style="padding-top: 66px;">
        <SectionTopBanner />
        <div class="">
            <div class="container my-5 pt-4">
                <p class="text-center">Our Equipment Builder Partnership fosters a collaborative and close-knit
                    relationship with engineering specialists across diverse industry sectors. These dynamic
                    partnerships are not just transactional—they drive innovation and lead to the development of
                    cutting-edge lubrication products tailored to the evolving needs of our clients. Just as Original
                    Equipment Manufacturers (OEMs) rely on us to provide unparalleled lubrication expertise throughout
                    the entire life cycle of their equipment—from design and testing to operation and maintenance—we, in
                    turn, depend on their valuable insights and feedback. This collaboration allows us to continuously
                    improve and refine our lubricants and related services to ensure they meet the highest standards of
                    performance, efficiency, and reliability.By working hand-in-hand with OEMs, we stay ahead of
                    emerging trends and challenges, enabling us to offer solutions that not only optimize the
                    performance of today’s equipment but also anticipate the future needs of the industries we serve.
                    Our mutual commitment to excellence and innovation ensures that together, we deliver products and
                    services that maximize equipment uptime, enhance productivity, and reduce operational costs,
                    ultimately driving long-term success for our partners.
                </p>

            </div>
            <div class="d-none d-md-flex justify-content-center align-items-center gap-3 my-5">
                <button class="btn w-25" style="border:1px solid rgba(255, 0, 0, 1) !important;" @click="share">
                    <i class="bi bi-share me-2"></i>
                    <span>Share</span>
                </button>
                <button class="btn btn-danger d-flex justify-content-center align-items-center w-25"
                    data-bs-toggle="modal" data-bs-target="#oemEnquiry"><span> Enquiry </span><i
                        class="bi bi-arrow-right ms-2"></i>
                </button>
            </div>
            <div class="position-fixed bottom-0 w-100 btn-group d-flex d-md-none" style="z-index:10">
                <button class="btn btn-danger w-25 rounded-0" @click="share"><i class="bi bi-share fs-2"></i></button>
                <button class="btn btn-danger w-75 rounded-0 d-flex align-items-center justify-content-between"
                    data-bs-toggle="modal" data-bs-target="#oemEnquiry">
                    <span class="ms-3 fs-5 text-uppercase">Enquiry Now</span>
                    <i class="bi bi-arrow-right ms-2 fs-1"></i>
                </button>
            </div>
            <div class="container my-5 pt-4">
                <h1 class="text-center mb-5 fw-bold">Unlock Strategic Resources to Elevate Your Brand</h1>
                <div class="row">
                    <div v-for="(step, index) in steps" :key="index" class="col-md-3 mb-4">
                        <div class="d-flex gap-2 align-items-center border rounded-5 border-start-0"
                            style="background-color:rgba(255, 0, 0, 0.2); border:1px solid rgba(255, 0, 0, 1) !important;border-radius: 3rem !important;">
                            <div class="bg-dark text-danger border d-flex justify-content-center align-items-center fs-1 rounded-circle"
                                style="min-width: 80px; height: 80px;">{{ index + 1 }}</div>
                            <p class="text-start mb-0 small">{{ step.title }}</p>

                        </div>
                    </div>
                </div>
            </div>
            <div class="container my-5">
                <p class="text-center fs-1 fw-bold p-2  text-capitalize">About CLG oil & greases</p>
                <p class="text-start">CLG Oil & Greases are high-performance lubricants specifically engineered to
                    address the unique needs of various engines and machinery. These products are developed through
                    rigorous field testing and advanced formulation techniques to ensure optimal performance. CLG Oil is
                    designed to significantly reduce engine wear, extend the lifespan of engine components, and increase
                    the intervals between oil changes. This results in superior protection and efficiency, making it a
                    reliable choice for maintaining engine health and performance.
                </p>

            </div>


            <div class="container my-5">
                <p class="text-center fs-1 fw-bold p-2 text-capitalize">Why Choose CLG oil & greases</p>
                <div class="row">
                    <p class="text-start col-md-6">
                        While many oils might seem similar at first glance, their performance can vary greatly. CLG Oil
                        & Greases are formulated to offer exceptional protection and efficiency that generic oils often
                        cannot match. Unlike standard oils that meet general performance standards such as API service
                        categories or IS specifications, CLG Oil exceeds these basic benchmarks. It is meticulously
                        tailored to meet the specific demands of different engines and equipment. This means enhanced
                        protection, reduced wear, and longer service intervals, which translates to fewer maintenance
                        issues and improved performance. Original Equipment Manufacturers (OEMs) recommend CLG Oil due
                        to its superior formulation, which ensures reliability and longevity for their engines. This
                        specialized approach helps in reducing overall maintenance costs and achieving better engine
                        performance.
                    </p>
                    <div class="col-md-6">
                        <img src="/img/about/oilpouring.jpeg" alt="text.heading" class="img-fluid" />
                    </div>
                </div>
            </div>
            <div class="container my-5">
                <div class="row mt-5">
                    <div class="col-md-6" v-for="(data, index) in datas" :key="index">
                        <div class="p-2 data-overlay" style="background-image:url('/img/gear.png')">
                            <h2 class="text-start fs-1 fw-bold p-2 text-capitalize">{{ data.title }}</h2>
                            <ul v-if="data.points" class="text-start">
                                <li v-for="(point, index) in data.points" :key="index" class="mb-2">{{ point }}</li>
                            </ul>
                        </div>
                    </div>
                    <p class="text-center my-5">With the growing customer expectations in terms of longer equipment
                        life,
                        fuel economy, reliability
                        in service and complying with prevalent emission norms, it has become necessary particularly for
                        prestigious OEMs. OEMs recommend use of their CLG Oils as it reduces warranty claims and
                        enhances brand equity.</p>
                </div>
            </div>
            <div class="container my-5">
                <div class="row justify-content-center align-items-center">
                    <p class="text-center fs-1 fw-bold p-2 text-capitalize mb-5">Our Offerings For OEM's</p>
                    <div class="col-md-6">
                        <img src="/img/oem.jpeg" class="w-75" alt="OEM">
                    </div>
                    <div class="col-md-6">
                        <ul class="text-start">
                            <li v-for="(point, index) in points" :key="index" class="mb-2 fs-4">{{ point }}</li>
                        </ul>
                    </div>

                </div>
            </div>
        </div>

        <div class="modal fade" id="oemEnquiry" tabindex="-1" aria-labelledby="oemEnquiryLabel" aria-hidden="true">
            <div class="modal-dialog  modal-dialog-centered">
                <div class="modal-content position-relative">
                    <div class="modal-header border-0 pt-4">
                        <h1 class="modal-title fs-5" id="oemEnquiryLabel">{{ pageName }}</h1>
                    </div>
                    <div class="position-absolute rounded-circle wh-40 bg-danger text-white px-2 p-1 end-0"
                        data-bs-dismiss="modal" style="top: -3%;">
                        <i class="bi bi-x fs-5"></i>
                    </div>
                    <div class="modal-body">
                        <form @submit.prevent="sendToWhatsApp()" class="row g-3 needs-validation" novalidate>
                            <div class="w-100 form-floating my-2">
                                <input type="text" class="form-control" placeholder="" v-model="name" required>
                                <label for="floatingInput" class="text-muted ms-2">Name</label>
                            </div>
                            <div class="w-100 form-floating my-2">
                                <textarea class="form-control" placeholder="Leave a comment here" id="floatingTextarea"
                                    v-model="note"></textarea>
                                <label for="floatingTextarea" class="ms-2 text-muted">Notes...</label>
                            </div>
                            <button
                                class="d-flex justify-content-center align-items-center btn btn-success text-uppercase p-0 py-1"
                                data-bs-dismiss="modal"><i class="bi bi-whatsapp fs-5 me-4"></i> <span class="fs-5">
                                    Enquiry Now</span></button>

                        </form>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import SectionTopBanner from "@/components/SectionTopBanner.vue"

export default {
    components: {
        SectionTopBanner,
    },
    data() {
        return {
            texts: [
                {
                    heading: "OEM solutions",
                    text: "Our Equipment Builder Partnership fosters a collaborative and close-knit relationship with engineering specialists across diverse industry sectors. These dynamic partnerships are not just transactional—they drive innovation and lead to the development of cutting-edge lubrication products tailored to the evolving needs of our clients. Just as Original Equipment Manufacturers (OEMs) rely on us to provide unparalleled lubrication expertise throughout the entire life cycle of their equipment—from design and testing to operation and maintenance—we, in turn, depend on their valuable insights and feedback. This collaboration allows us to continuously improve and refine our lubricants and related services to ensure they meet the highest standards of performance, efficiency, and reliability.By working hand-in-hand with OEMs, we stay ahead of emerging trends and challenges, enabling us to offer solutions that not only optimize the performance of today’s equipment but also anticipate the future needs of the industries we serve. Our mutual commitment to excellence and innovation ensures that together, we deliver products and services that maximize equipment uptime, enhance productivity, and reduce operational costs, ultimately driving long-term success for our partners.",
                },
                {
                    heading: "What is CLG oil?",
                    text: "CLG Oil is a highly specialized, tailor-made lubricant, meticulously developed after extensive field trials to meet the precise requirements of specific engines. It is engineered to deliver exceptional performance in areas such as reduced engine component wear, extended engine rebuild life, and prolonged drain service intervals, ensuring superior protection and efficiency."
                },
                {
                    heading: "",
                    text: "",
                    image: "https://www.velvex.in/images/adBlue/goGreen/Why-CLG-Oil.jpg",
                },
            ],
            datas: [
                {
                    "title": "Performance Benefits of CLG Oil",
                    "points": [
                        "Enhances engine rebuild life",
                        "Ensures peak performance for long",
                        "Customized product to meet engine aptitude",
                        "Reduced maintenance cost",
                        "Strengthens brand equity",
                        "Extends drain service intervals",
                        "An all-round the year oil",
                        "Total engine protection during working and idle period",
                        "Reduced down time and increased profits"
                    ]
                },
                {
                    "title": "Performance Benefits of CLG Grease",
                    "points": [
                        "Provides excellent wear protection in extreme conditions",
                        "Ensures high thermal stability under varying loads",
                        "Resists water washout in wet environments",
                        "Enhances equipment life through superior lubrication",
                        "Reduces downtime and maintenance costs",
                        "Prevents rust and corrosion on metallic surfaces",
                        "Offers high load-carrying capacity for heavy-duty applications",
                        "Improves mechanical efficiency in bearings and joints",
                        "Ensures consistent performance in both high and low temperatures"
                    ]
                },
            ],

            points: [
                "Lubrication Technology Consultation",
                "Shared Technical Trends, Information",
                "Consistent Worldwide Performance Standards",
                "Field Engineering Support and Liaison",
                "Reliable Nationwide Supply",
                "Ethical Business Relationship"
            ],
            steps: [
                { title: 'Product and Market Knowledge', },
                { title: 'Assistance in Choosing Formulations', },
                { title: 'Product Development', },
                { title: 'Support with product and safety information', },
                { title: 'Brand Development, Design and Copywriting', },
                { title: 'Assistance in Choosing packaging', },
                { title: 'Logistics', },
            ],
            note: '',
            name: '',
        };
    },
    methods: {
        share() {
            if (navigator.share) {
                navigator.share({
                    title: 'Share this content',
                    text: 'Check out this awesome content!',
                    url: window.location.href,
                }).then(() => {
                    console.log('Successful share');
                }).catch((error) => {
                    console.log('Error sharing', error);
                });
            } else {
                alert('Web Share API is not supported in your browser.');
            }
        },
        sendToWhatsApp() {
            const phoneNumber = '919711256073';
            const message = `Name: ${this.name}%0A
            Note: ${this.note}`;

            const url = `https://wa.me/${phoneNumber}?text=${message}`;
            window.open(url, '_blank');
        },
    }
};
</script>

<style scoped>
.data-overlay {
    background-color: var(--bg-primary);
    background-repeat: no-repeat;
    background-position: bottom right;
    background-size: 150px;
    position: relative;
    overflow: hidden;
}

.data-overlay::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: 1;
}

.data-overlay h2,
.data-overlay ul {
    position: relative;
    z-index: 2;
    color: #fff;
}
</style>