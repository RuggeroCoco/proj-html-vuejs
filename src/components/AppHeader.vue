<script>
export default {
  name: "AppHeader",
  data() {
    return {
      openingHours: "Open Hours: Mon - Sat - 9:00 - 18:00",
      contacts: {
        phone: "+1(305)1234-5678",
        email: "hello@example.com",
      },
    };
  },
};
</script>

<template>
  <!-- HEAD-BAR -->
  <div class="head-bar d-flex justify-content-between">
    <div class="head-bar--left">
      <i class="fa-solid fa-clock me-2"></i><span>{{ openingHours }}</span>
    </div>
    <div class="head-bar--right">
      <a :href="'tel:' + contacts.phone">
        <i class="fa-solid fa-phone me-2"></i
        ><span class="me-3">{{ contacts.phone }}</span>
        </a>
        <a :href="'mailto:' + contacts.email">
      <i class="fa-solid fa-envelope me-2"></i
      ><span class="me-3">{{ contacts.email }}</span>
      </a>
      <a href="/"><i class="fa-brands fa-facebook-f me-3"></i></a>
      <a href="/"><i class="fa-brands fa-twitter me-3"></i></a>
      <a href="/"><i class="fa-brands fa-linkedin-in"></i></a>
    </div>
  </div>
  <!-- HEAD-BAR -->
  <!-- HEAD-MENU -->
  .head-menu
</template>

<style scoped lang="scss">
.head-bar {
  background-color: #24333d;
  padding: 0.8rem 17rem;
  &--left,
  &--right {
    color: #e3e7df;
    font-size: 13px;
  }
  a {
    text-decoration: none;
    color: #e3e7df;
  }
}
</style>
