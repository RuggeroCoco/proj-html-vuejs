<script>
export default {
  props: {
    items: []
  },
};
</script>

<template>
  <div class="features-container">
    <div class="feature" v-for="(item, index) in items" :key="index">
      <i :class="'fa-solid  ' + item.icon"></i>
      <h3 class="title"> {{ item.title }}</h3>
      <p class="description"> {{ item.description }}</p>
    </div>
  </div>
</template>

<style scoped lang="scss">
.features-container {
  display: flex;
  justify-content: center;
  background-color: #e3e7df;
  width: 100%;
  padding: 6rem 0;

  i {
    color: #0d7e7e;
    padding: 1rem;
    background-color: #e3e7df;
    border-radius: 50%;
    margin-bottom: 1rem;
  }
}

.feature {
  padding: 2rem 2rem;
  background-color: white;
  border-radius: 10px;
  max-width: 20%;

  &:not(:last-child) {
    margin-right: 1rem;
  }
}
</style>
