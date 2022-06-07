<template>
  <nav class="navbar">
    <div class="navbar-links">
      <ul>
        <a href="#"
          ><li>{{ about }}</li></a
        >
      </ul>
    </div>

    <a href="#" class="toggle-button">
      <span class="bars"></span>
      <span class="bars bar-one"></span>
    </a>
    <div class="logo">
      <a href="">{{ title }}</a>
    </div>
    <div class="navbar-links">
      <ul>
        <a href="#"
          ><li>{{ contact }}</li></a
        >
      </ul>
    </div>
  </nav>
</template>

<script>
import "../components/styles/global.css";
import gsap from "gsap";
export default {
  name: "Navbar",
  //The props are declared in here for you to use them in the component
  props: ["title", "about", "contact"],
};
</script>

<style scoped>
.navbar {
  display: flex;
  justify-content: space-between;
  padding: 1.5rem 2rem;
}

.logo {
  font-family: "Aeonik Black", sans-serif;
  font-size: clamp(3rem, 5vw + 1rem, 8rem);
  margin-top: -1rem;
  text-transform: uppercase;
  user-select: none;
  -moz-user-select: none;
  display: inline-block;
}

.navbar .navbar-links a li {
  font-size: clamp(1rem, 0.5vw + 1rem, 1.5rem);
  text-transform: uppercase;
}

.navbar .navbar-links a li::selection {
  background: #fff;
  color: #ff0000;
}

.toggle-button {
  position: absolute;
  top: 3.3rem;
  right: 2rem;
  display: none;
  flex-direction: column;
  justify-content: space-between;
  width: 4rem;
  height: 1.5rem;
  text-align: right;
}

.toggle-button .bars {
  height: 4px;
  width: 100%;
  background-color: #000000;
}
.toggle-button .bar-one {
  height: 4px;
  width: 80%;
  background-color: #000000;
  align-self: flex-end;
}

@media (max-width: 40em) {
  .navbar .navbar-links {
    display: none;
  }
  .navbar {
    align-items: left;
    padding: 2rem 1rem;
  }
  .navbar .logo {
    margin-top: 0;
  }

  .toggle-button {
    display: flex;
  }
}
</style>
