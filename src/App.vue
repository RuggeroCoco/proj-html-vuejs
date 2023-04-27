<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";

export default {
  components: { AppHeader, AppMain },
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
    };
  },
};
</script>

<template>
  <AppHeader :items="menuItems" />
  <AppMain />
</template>

<style scoped></style>
