<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/Hero.vue";
import Features from "./components/Features.vue"

export default {
  components: { AppHeader, AppMain, Features },
  data() {
    return {
      menuItems: [
        {
          label: "HOME",
          url: "/",
        },
        {
          label: "ABOUT",
          url: "/",
        },
        {
          label: "SERVICES",
          url: "/",
        },
        {
          label: "ABOUT",
          url: "/",
        },
        {
          label: "BLOG",
          url: "/",
        },
        {
          label: "GET IN TOUCH",
          url: "/",
        },
      ],
      features: [
        {
          icon: "fa-user-group",
          title: "Human Capital",
          description: "Humanizing business: Harness the power of technology to improve the way people work"
        },
        {
          icon: "fa-chart-pie",
          title: "Core Business",
          description: "It takes innovative approaches to trasform",
        },
        {
          icon: "fa-gauge-high",
          title: "Performance",
          description: "Achieving maximum impact and value from investments in finance and supply chain",
        },
      ],
    };
  },
};
</script>

<template>
  <AppHeader :items="menuItems" />
  <AppMain />
  <Features :items="features" />
</template>

<style scoped></style>
