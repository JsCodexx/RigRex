<template>
  <ceiling-defination></ceiling-defination>
  <ceiling-uses></ceiling-uses>
  <stretch-ceiling-installation></stretch-ceiling-installation>
  <types-of-ceiling></types-of-ceiling>
  <ceiling-charactristics-card-vue></ceiling-charactristics-card-vue>
  <ceiling-installation-card></ceiling-installation-card>
  <appointment-card></appointment-card>
  <!-- <carousel-card></carousel-card> -->
  <!-- <ceiling-card></ceiling-card>
  <intro-card></intro-card>
  <privacy-card></privacy-card>
  <ceiling-video></ceiling-video> -->
  <!-- <social-stream-slce-vue></social-stream-slce-vue> -->
</template>

<script>
import CeilingDefination from "./components/CeilingDefination.vue";
import CeilingUses from "./components/CeilingUses.vue";
import StretchCeilingInstallation from './components/StretchCeilingInstallation.vue';
import TypesOfCeiling from "./components/TypesOfCeiling.vue";
import AppointmentCard from "./components/AppointmentCard.vue";
import CeilingCharactristicsCardVue from "./components/CeilingCharactristicsCard.vue";
import CeilingInstallationCard from "./components/CeilingInstallationCard.vue";
// import SocialStreamSlceVue from './components/SocialStreamSlce.vue';
// import CarouselCard from "@/components/CarouselCard"
// import IntroCard from "@/components/IntroCard";
// import PrivacyCard from "@/components/PrivacyCard.vue";
// import CeilingCard from "./components/CeilingCard.vue";
// import CeilingVideo from "./components/CeilingVideo.vue"
export default {
  name: "App",
  components: {
    // IntroCard,
    // PrivacyCard,
    // CeilingCard,
    // CeilingVideo ,
    // CarouselCard,
    // SocialStreamSlceVue
    CeilingInstallationCard,
    CeilingCharactristicsCardVue,
    CeilingDefination,
    CeilingUses,
    AppointmentCard,
    StretchCeilingInstallation,
    TypesOfCeiling,
  },
};
</script>

<style></style>
