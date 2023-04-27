<script>
export default {
  name: "AppHeader",
  props: {
    items: [],
  },
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
  <div class="header">
    <div class="header-contacts d-flex justify-content-between">
      <div class="header-contacts-left">
        <i class="fa-solid fa-clock me-2"></i><span>{{ openingHours }}</span>
      </div>
      <div class="header-contacts-right">
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
    <div class="header-menu d-flex justify-content-between">
      <div><img src="../assets/images/logo.png" alt="" /></div>
      <div class="d-flex">
        <div v-for="item in items" :key="item.label">
          <a :href="item.url">{{ item.label }}</a>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.header {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
}
.header-contacts {
  background-color: #24333d;
  padding: 0.8rem 17rem;
  &-left,
  &-right {
    color: #e3e7df;
    font-size: 13px;
  }
  a {
    text-decoration: none;
    color: #e3e7df;
  }
}

.header-menu {
  align-items: center;
  padding: 0.8rem 17rem;
  a {
    text-decoration: none;
    color: white;
    transition: all 300ms;
    padding: 0.5rem;
    &:not(:last-child) {
      margin-right: 1rem;
    }
  }
  a:hover {
    background-color: #0d7e7e;
    border-radius: 5px;
  }
}
</style>
