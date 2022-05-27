<template>
  <div>
    <Navbar :title="title" :about="about" :contact="contact" />
    <Header />
  </div>
</template>

<script>
import "../components/styles/global.css";
import "../components/styles/base.css";
import Navbar from "../components/Navbar.vue";
import Header from "../components/Header.vue";

export default {
  name: "IndexPage",

  //The components put together to make one application in the app component
  components: { Navbar, Header },
  //Data object to return all the data in this component
  data() {
    return {
      //props in the header component
      title: "Calvin",
      about: "about",
      contact: "contact",
    };
  },
};
</script>
