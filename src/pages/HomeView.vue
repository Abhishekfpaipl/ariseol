<template>
  <div class="mt-2">
    <GallerySection />
    <CounterSection />
    <CardSection />
    <ImageTextSection />
  </div>
</template>

<script>
import GallerySection from "@/components/GallerySection.vue";
import CounterSection from "@/components/CounterSection.vue";
import CardSection from "@/components/CardSection.vue";
import ImageTextSection from "@/components/ImageTextSection.vue";

export default {
  name: "HomeView",
  components: {
    GallerySection,
    CounterSection,
    CardSection,
    ImageTextSection,
  },
};
</script>
