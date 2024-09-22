<template>
  <div class="mt-2" style="padding-top: 64px;">
    <CarouselBanner />
    <CardSection />
    <ImageSection />

    <ImageTextSection image-src="/img/gallery/1.jpg" heading="High-Performance Industrial Oils for Enhanced Efficiency"
      subHeading="Our range of industrial oils is designed to meet the demands of various industries, offering superior lubrication, reduced friction, and enhanced equipment longevity."
      :points="points" image-alt="gallery" :imageFirst="true" />

    <ImageTextSection image-src="/img/gallery/10.jpg" heading="Advanced Industrial Grease for Heavy-Duty Applications"
      subHeading="Our industrial greases are engineered to provide superior protection and performance in
                    the most demanding environments, ensuring machinery runs smoothly and efficiently." text="Formulated to withstand extreme temperatures and high loads, our grease minimizes friction, reduces
                    wear, and extends the lifespan of your equipment. It offers excellent water resistance and corrosion
                    protection, making it ideal for industrial applications such as manufacturing, mining, and
                    construction." image-alt="gallery" :imageFirst="false" />

    <ImageTextSection image-src="/img/gallery/3.jpg" heading="Leaders in Oil and Grease Manufacturing" subHeading="Our industry is at the forefront of producing high-performance oils and greases that
                    meet the demands of various sectors, from automotive to heavy machinery and industrial equipment."
      text="We specialize in advanced formulations that enhance machinery efficiency, reduce wear, and extend the
                    lifespan of equipment. Our products are designed to operate under extreme conditions, providing
                    reliable lubrication, protection against corrosion, and optimal performance for a wide range of
                    applications. With a focus on sustainability, we continuously innovate to deliver solutions that
                    help reduce energy consumption and environmental impact." image-alt="gallery"
      :imageFirst="true" />

    <!-- <ImageTextSection /> -->
    <GermanTechonology />
    <GermanPerformance />
    <ProductSection />
    <FeaturesSection />
    <WeAreAriseol />
    <OurAdvantages />
    <AboutSection />
    <GallerySection />
    <TeamSection />
    <TestimonialSection />
    <ContactSection />
  </div>
</template>

<script>
import CarouselBanner from "@/components/CarouselBanner.vue";
import GallerySection from "@/components/GallerySection.vue";
import CardSection from "@/components/CardSection.vue";
import ImageTextSection from "@/components/ImageTextSection.vue";
import ProductSection from "@/components/ProductSection.vue";
import TeamSection from "@/components/TeamSection.vue";
import ContactSection from "@/components/ContactSection.vue";
import AboutSection from "@/components/AboutSection.vue";
import TestimonialSection from "@/components/TestimonialSection.vue";
import ImageSection from "@/components/ImageSection.vue";
import FeaturesSection from "@/components/FeaturesSection.vue";
import WeAreAriseol from "@/components/WeAreAriseol.vue";
import OurAdvantages from "@/components/OurAdvantages.vue";
import GermanTechonology from "@/components/GermanTechonology.vue";
import GermanPerformance from "@/components/GermanPerformance.vue";

export default {
  name: "HomeView",
  components: {
    CarouselBanner,
    GallerySection,
    ImageSection,
    CardSection,
    ImageTextSection,
    ProductSection,
    TeamSection,
    ContactSection,
    AboutSection,
    TestimonialSection,
    FeaturesSection,
    WeAreAriseol,
    OurAdvantages,
    GermanTechonology,
    GermanPerformance,
  },
  data() {
    return {
      points: [
        "Optimized for heavy-duty machinery, ensuring smooth operation under extreme conditions.",
        "Formulated to reduce energy consumption and minimize equipment wear.",
        "Provides superior protection against rust, corrosion, and oxidation."
      ]
    };
  }
};
</script>
