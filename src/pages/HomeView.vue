<template>
  <div class="mt-2" style="padding-top: 74px;">
    <CounterSection />
    <CardSection />
    <ImageTextSection />
    <GallerySection />
    <TeamSection />
    <ContactSection />
  </div>
</template>

<script>
import GallerySection from "@/components/GallerySection.vue";
import CounterSection from "@/components/CounterSection.vue";
import CardSection from "@/components/CardSection.vue";
import ImageTextSection from "@/components/ImageTextSection.vue";
import TeamSection from "@/components/TeamSection.vue";
import ContactSection from "@/components/ContactSection.vue";

export default {
  name: "HomeView",
  components: {
    GallerySection,
    CounterSection,
    CardSection,
    ImageTextSection,
    TeamSection,
    ContactSection,
  },
};
</script>
