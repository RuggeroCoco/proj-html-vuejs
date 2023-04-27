<script>
export default {
  name: "Hero",
};
</script>

<template>
  <div class="hero">
    <div class="hero-content">
      <h2>Lead ~ Customer</h2>
      <p>
        Successful strategies require data analysis, creativity and customer
        focus, taking advantage of the latest technologies to offer excellent
        services.
      </p>
      <div>
        <input type="button" value="GET IN TOUCH" class="button me-3" />
        <input type="button" value="READ MORE" class="button" />
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.hero {
  display: flex;
  align-items: center;
  justify-content: center;
  background-image: url(../assets/images/hero-image.png);
  background-size: cover;
  background-repeat: no-repeat;
  box-shadow: inset 0 0 0 2000px rgba(0, 0, 0, 0.7);
  text-align: center;
  height: 100vh;

  &-content {
    max-width: 50%;
    padding: 1rem 0;
  }

  h2 {
    color: white;
    font-size: 3rem;
    font-weight: bold;
  }

  p {
    color: gray;
  }

  .button {
    border: 1px solid #0d7e7e;
    color: white;
    background-color: transparent;
    border-radius: 5px;
    padding: 0.2rem 0.8rem;
    transition: all 300ms;

    &:hover {
      background-color: #0d7e7e;
    }
  }
}
</style>
