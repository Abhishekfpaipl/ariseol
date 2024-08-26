<template>
  <div class="mt-2" style="padding-top: 74px;">
    <CounterSection />
    <CardSection />
    <ImageTextSection />
    <ProductSection />
    <AboutSection />
    <GallerySection />
    <TeamSection />
    <TimelineSection />
    <CareerSection />
    <ContactSection />
  </div>
</template>

<script>
import GallerySection from "@/components/GallerySection.vue";
import CounterSection from "@/components/CounterSection.vue";
import CardSection from "@/components/CardSection.vue";
import ImageTextSection from "@/components/ImageTextSection.vue";
import ProductSection from "@/components/ProductSection.vue";
import TeamSection from "@/components/TeamSection.vue";
import ContactSection from "@/components/ContactSection.vue";
import AboutSection from "@/components/AboutSection.vue";
import TimelineSection from "@/components/TimelineSection.vue";
import CareerSection from "@/components/CareerSection.vue";

export default {
  name: "HomeView",
  components: {
    GallerySection,
    CounterSection,
    CardSection,
    ImageTextSection,
    ProductSection,
    TeamSection,
    ContactSection,
    AboutSection,
    TimelineSection,
    CareerSection,
  },
};
</script>
