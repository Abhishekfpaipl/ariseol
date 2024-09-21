<template>
  <div class="mt-2" style="padding-top: 64px;">
    <CarouselBanner />
    <!-- <CardSection /> -->
    <ImageTextSection />
    <ProductSection />
    <AboutSection />
    <GallerySection />
    <TeamSection />
    <TestimonialSection />
    <CareerSection />
    <ContactSection />
  </div>
</template>

<script>
import CarouselBanner from "@/components/CarouselBanner.vue";
import GallerySection from "@/components/GallerySection.vue";
// import CardSection from "@/components/CardSection.vue";
import ImageTextSection from "@/components/ImageTextSection.vue";
import ProductSection from "@/components/ProductSection.vue";
import TeamSection from "@/components/TeamSection.vue";
import ContactSection from "@/components/ContactSection.vue";
import AboutSection from "@/components/AboutSection.vue";
import TestimonialSection from "@/components/TestimonialSection.vue";
import CareerSection from "@/components/CareerSection.vue";

export default {
  name: "HomeView",
  components: {
    CarouselBanner,
    GallerySection,
    // CardSection,
    ImageTextSection,
    ProductSection,
    TeamSection,
    ContactSection,
    AboutSection,
    CareerSection,
    TestimonialSection,
  },
};
</script>
