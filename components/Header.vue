<template>
  <div>
    <div class="header-container">
      <hr />
      <div class="position">
        <h3>Mobile App Developer</h3>
      </div>
      <div class="about">
        <p>
          Hi, I’m Calvin I am <br />
          a app developer. I<br />
          create the best modern <br />
          applications for all types of<br />
          businesses and people.
        </p>
      </div>
      <div class="image-container">
        <img
          class="fade-image"
          src="https://images.unsplash.com/photo-1521119989659-a83eee488004?crop=entropy&cs=tinysrgb&fm=jpg&ixlib=rb-1.2.1&q=80&raw_url=true&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=423"
          alt=""
        />
      </div>

      <div class="title-container">
        <h3 class="calvin">
          Calvin <br />
          Mathiba
        </h3>
      </div>
    </div>
  </div>
</template>

<script>
import { gsap } from "gsap";

export default {
  name: "Header",
  mounted() {
    // gsap.from(".calvin", { opacity: 0, duration: 1, y: 50, stagger: 0.6 });

    const tl = gsap.timeline({ defaults: { duration: 1.5 } });

    tl.from(".calvin", { opacity: 0, y: 50 }).from(
      ".about",
      { opacity: 0, y: -30 },
      "-=.5"
    );
  },
};
</script>

<style scoped>
.header-container {
  position: relative;
  padding: 0 2rem;
}

.header-container .about {
  position: absolute;
  top: 10.5rem;
  right: 3rem;
  font-family: "Aeonik Regular", sans-serif;
  font-weight: lighter;
}

.position h3 {
  position: absolute;
  top: 20%;
  left: 50%;
  transform: translate(-13.2rem, 7rem);
  font-size: clamp(1rem, 1vw + 0.7rem, 2.5rem);
}

.header-container .image-container {
  position: absolute;
  left: 50%;
  top: 60%;
  transform: translate(-50%, 30%);
  -webkit-user-select: none;
  user-select: none;
  -moz-user-select: none;
  display: inline-block;
  overflow: hidden;
  z-index: -2222;
}

.header-container .image-container img {
  object-fit: cover;
  max-width: 100%;
  user-select: none;
  -moz-user-select: none;
  -webkit-user-select: none;
  image-rendering: auto;
  -moz-image-rendering: auto;
  -webkit-image-rendering: auto;
  display: inline-block;
  pointer-events: none;
  z-index: -2222;
}

.header-container .title-container {
  position: absolute;
  top: 50%;
  transform: translate(0, 17rem);
}

.header-container .title-container h3 {
  font-family: "Aeonik Bold", sans-serif;
  font-size: clamp(4.5rem, 8.5vw + 1rem, 11rem);
  line-height: 0.8;
  letter-spacing: 0.5rem;
}

hr {
  top: 40%;
  right: 2.5%;
  width: 63%;
  transform: translate(0, 6rem);
  position: absolute;
  z-index: -5555;
  background-color: #000;
}

.header-container .title-container h3::selection {
  background: #fff;
  color: #ff0000;
}
.header-container .position h3::selection {
  background: #fff;
  color: #ff0000;
}
.header-container .about ::selection {
  background: #fff;
  color: #ff0000;
}

@media (max-width: 40em) {
  hr {
    width: 90%;
    transform: translate(-0.7rem, 1rem);
  }

  .header-container .about {
    display: none;
  }

  .header-container .image-container {
    width: 90%;
    transform: translate(-50%, 13rem);
  }

  .position h3 {
    transform: translate(-11rem, 1.5rem);
  }

  .header-container .title-container {
    transform: translate(-1rem, 4rem);
  }
}
</style>
