<template>
    <div class="position-fixed w-100 d-flex justify-content-between  align-items-center p-2 top-0"
        style="z-index: 10; background-color: var(--brand-color);">
        <img src="img/logo.png" alt="" style="height: 50px;">
        <div class="d-none d-md-flex align-items-center gap-3">
            <router-link :to="link.route" class="text-decoration-none text-white" v-for="(link, index) in links"
                :key="index">{{ link.name }}</router-link>
        </div>
        <i class="bi bi-list fs-1 d-md-none d-block text-white" data-bs-toggle="offcanvas" data-bs-target="#MobileMenu"
            aria-controls="MobileMenu"></i>
    </div>
    <div class="offcanvas offcanvas-end" tabindex="-1" id="MobileMenu" aria-labelledby="MobileMenuLabel">
        <div class="offcanvas-header">
            <h5 class="offcanvas-title" id="MobileMenuLabel">Offcanvas</h5>
            <button type="button" class="btn-close" data-bs-dismiss="offcanvas" aria-label="Close"></button>
        </div>
        <div class="offcanvas-body">
            <div class="d-flex flex-column align-items-start gap-3">
                <router-link :to="link.route" class="text-decoration-none text-dark" v-for="(link, index) in links"
                    :key="index">{{ link.name }}</router-link>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: "TopNav",
    data() {
        return {
            links: [
                { name: 'Home', route: '/' },
                { name: 'About Us', route: '/' },
                { name: 'Features', route: '/' },
                { name: 'Gallery', route: '/' },
                { name: 'Team', route: '/' },
                { name: 'Pricing', route: '/' },
                { name: 'Contact', route: '/' },
            ]
        }
    }
}
</script>
<style lang="">

</style>