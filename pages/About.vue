<template>
  <div class="home">
    <h1>{{ about }}</h1>
  </div>
</template>

<script>
export default {
  data() {
    return {
      about: "ABOUT",
    };
  },
};
</script>

<style scoped>
.home {
  text-align: center;
  font-size: 7.5rem;
}
h1 {
  position: relative;
  margin-top: 60rem;
  opacity: 7rem;
  user-select: none;
  -moz-user-select: none;
  -webkit-user-select: none;
  z-index: -111;
}
</style>
