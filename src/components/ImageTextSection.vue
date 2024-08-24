<template>
    <div class="container my-5">
        <h2 class="text-primary mb-5 text-start">CHECK OUR DETAILS</h2>
        <div class="row mb-5">
            <div class="col-md-6" v-observe :class="imageClass('left')">
                <img src="https://bootstrapmade.com/demo/templates/Bootslander/assets/img/details-2.png"
                    alt="Illustration" class="img-fluid">
            </div>
            <div class="col-md-6 d-flex flex-column justify-content-center" v-observe :class="textClass('right')">
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
        <div class="row">
            <div class="col-md-6 order-md-2" v-observe :class="imageClass('right')">
                <img src="https://bootstrapmade.com/demo/templates/Bootslander/assets/img/details-4.png"
                    alt="Illustration" class="img-fluid">
            </div>
            <div class="col-md-6 order-md-1 d-flex flex-column justify-content-center" v-observe
                :class="textClass('left')">
                <h3 class="text-primary mb-3">Corporis temporibus maiores provident</h3>
                <p class="mb-4">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
                    incididunt ut labore et dolore magna aliqua.</p>
                <p>Ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in
                    voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
                    proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
            </div>
        </div>
        
        <div class="row">
            <div class="col-md-6 order-md-2" v-observe :class="imageClass('left')">
                <img src="https://bootstrapmade.com/demo/templates/Bootslander/assets/img/details-3.png"
                    alt="Illustration" class="img-fluid">
            </div>
            <div class="col-md-6 order-md-1 d-flex flex-column justify-content-center" v-observe
                :class="textClass('left')">
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
