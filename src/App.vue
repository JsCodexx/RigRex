<template>
  <ceiling-card></ceiling-card>
  <intro-card></intro-card>
  <privacy-card></privacy-card>
  <ceiling-video></ceiling-video>
</template>

<script>
import IntroCard from "@/components/IntroCard";
import PrivacyCard from "@/components/PrivacyCard.vue";
import CeilingCard from "./components/CeilingCard.vue";
import CeilingVideo from "./components/CeilingVideo.vue"
export default {
  name: "App",
  components: {
    IntroCard,
    PrivacyCard,
    CeilingCard,
    CeilingVideo ,
  },
};
</script>

<style>
</style>
