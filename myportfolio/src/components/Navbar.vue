<template>
  <div class="navbar">
    <div class="link-wrap">
      <router-link to="/" class="route-link">Home</router-link>
      <router-link to="/about" class="route-link">About</router-link>
      <router-link to="/resume" class="route-link">Resume</router-link>
      <router-link to="/projects" class="route-link">Projects</router-link>
      <router-link to="/contact" class="route-link">Contacts</router-link>
    </div>
  </div>
</template>

//
<script>
import Home from "../views/Home.vue";
import About from "../views/About.vue";
import Resume from "../views/Resume.vue";
import Projects from "../views/Projects.vue";
import Contact from "../views/Contact.vue";
export default {
  name: "Navbar",
  components: Home,
  About,
  Resume,
  Projects,
  Contact,
};
</script>

//
<!-- Add "scoped" attribute to limit CSS to this component only -->
//
<style scoped lang="scss">
.navbar {
  position: relative;
  max-width: 1440px;
  margin: 0 auto;
  padding: 12px 0;

  .link-wrap {
    position: fixed;
    display: flex;
    justify-content: space-between;
    width: 50%;
    align-items: center;
    top: 30px;
    left: 300px;

    .route-link {
      text-decoration: none;
      color: #fff;
      font-size: 14px;
      font-weight: 400;
    }
  }
}
</style>
