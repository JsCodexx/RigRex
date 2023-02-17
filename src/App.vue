<template>
  <ceiling-card></ceiling-card>
  <intro-card></intro-card>
  <privacy-card></privacy-card>
</template>

<script>
import IntroCard from "@/components/IntroCard";
import PrivacyCard from "@/components/PrivacyCard.vue";
import CeilingCard from "./components/CeilingCard.vue";
export default {
  name: "App",
  components: {
    IntroCard,
    PrivacyCard,
    CeilingCard,
  },
};
</script>

<style>
</style>
