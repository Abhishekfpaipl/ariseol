<template>
    <div class="container my-5">
        <h2 class="text-primary mb-5 text-start display-5">CHECK OUR DETAILS</h2>
        <div class="row mb-5">
            <div class="col-md-6" v-observe :class="imageClass('right')">
                <img src="https://img.freepik.com/premium-photo/oil-pump-setting-sun-oil-industry-fossil-fuel-extraction-industrial-sunset-landscape_436068-5121.jpg?w=996"
                    alt="Illustration" class="img-fluid">
                <!-- freepik link -->
                <!-- https://www.freepik.com/premium-ai-image/oil-pump-setting-sun-oil-industry-fossil-fuel-extraction-industrial-sunset-landscape_281849067.htm#fromView=search&page=2&position=20&uuid=2f873023-c4ef-479f-8c64-155a5ba5a7f0 -->
                <!-- freepik link -->

            </div>
            <div class="col-md-6 d-flex flex-column justify-content-center mt-4 mt-md-0 text-start" v-observe
                :class="textClass('right')">
                <h3 class="text-primary mb-3">Voluptatem dignissimos provident quasi corporis voluptates sit assumenda.
                </h3>
                <p class="mb-4">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
                    incididunt ut labore et dolore magna aliqua.</p>
                <ul class="list-unstyled">
                    <li class="mb-2">
                        <i class="bi bi-check2 text-primary me-2"></i>
                        Ullamco laboris nisi ut aliquip ex ea commodo consequat.
                    </li>
                    <li class="mb-2">
                        <i class="bi bi-check2 text-primary me-2"></i>
                        Duis aute irure dolor in reprehenderit in voluptate velit.
                    </li>
                    <li class="mb-2">
                        <i class="bi bi-check2 text-primary me-2"></i>
                        Ullamco laboris nisi ut aliquip ex ea commodo consequat.
                    </li>
                </ul>
            </div>
        </div>

        <!-- Second Row -->
        <div class="row mb-5">
            <div class="col-md-6 order-md-2" v-observe :class="imageClass('right')">
                <img src="https://img.freepik.com/free-vector/oil-prices-industry_24877-50042.jpg?t=st=1724484767~exp=1724488367~hmac=e2b1da6e9b755b0e30bec0eedc2f75509776ae2063a4b6fe7112566a3966d631&w=740"
                    alt="Illustration" class="img-fluid">

                <!-- freepik link -->
                <!--https://www.freepik.com/free-vector/oil-prices-industry_4875124.htm#fromView=search&page=2&position=21&uuid=2f873023-c4ef-479f-8c64-155a5ba5a7f0 -->
                <!-- freepik link -->
            </div>
            <div class="col-md-6 order-md-1 d-flex flex-column justify-content-center text-start" v-observe
                :class="textClass('left')">
                <h3 class="text-primary mb-3">Corporis temporibus maiores provident</h3>
                <p class="mb-4">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
                    incididunt ut labore et dolore magna aliqua.</p>
                <p>Ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in
                    voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
                    proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
            </div>
        </div>

        <div class="row mb-5">
            <div class="col-md-6" v-observe :class="imageClass('left')">
                <img src="https://img.freepik.com/premium-photo/hand-with-red-glove-that-has-liquid-dripping-out-it_605423-153131.jpg?w=996"
                    alt="Illustration" class="img-fluid">

                <!-- freepik link -->
                <!-- https://www.freepik.com/premium-ai-image/hand-with-red-glove-that-has-liquid-dripping-out-it_247544512.htm#fromView=search&page=1&position=27&uuid=66ade2e6-0f2b-4b6b-9489-dbca381bbf7a -->
                <!-- freepik link -->

            </div>
            <div class="col-md-6 d-flex flex-column justify-content-center text-start" v-observe
                :class="textClass('right')">
                <h3 class="text-primary mb-3">Corporis temporibus maiores provident</h3>
                <p class="mb-4">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
                    incididunt ut labore et dolore magna aliqua.</p>
                <p>Ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in
                    voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
                    proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ImageTextSection',
    methods: {
        imageClass(position) {
            return {
                'before-enter-right': position === 'right',
                'before-enter-left': position === 'left'
            };
        },
        textClass(position) {
            return {
                'before-enter-left': position === 'right',
                'before-enter-right': position === 'left'
            };
        }
    }
}
</script>

<style scoped>
.before-enter-left {
    opacity: 0;
    transform: translateX(-80px);
    transition: opacity 1.5s ease-out, transform 1.5s ease-out;
}

.before-enter-right {
    opacity: 0;
    transform: translateX(80px);
    transition: opacity 1.5s ease-out, transform 1.5s ease-out;
}

.enter {
    opacity: 1;
    transform: translateX(0);
}
</style>
