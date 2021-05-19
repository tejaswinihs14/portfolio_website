<template>
  <div class="home">
    <Navbar />
    <section class="home" id="home">
      <div class="max-width">
        <div class="home-content">
          <div class="text-1">Hello, my name is</div>
          <div class="text-2">Tejaswini</div>
          <div class="text-4">Helagalli Shivabasappa</div>
          <div class="text-3">And I'm a <span v-bind="typing"></span></div>
          <a href="#">Hire me</a>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";

export default {
  name: "Home",
  components: {
    Navbar,
  },
  methods: {
    // typed: new Typed(".typing", {
    typing: {
      strings: ["YouTuber", "Developer", "Blogger", "Designer", "Freelancer"],
      typeSpeed: 100,
      backSpeed: 60,
      loop: true,
    },
  },
};
</script>

<style scoped lang="scss">
section .title {
  position: relative;
  text-align: center;
  font-size: 40px;
  font-weight: 500;
  margin-bottom: 60px;
  padding-bottom: 20px;
  font-family: "Ubuntu", sans-serif;
}
section .title::before {
  content: "";
  position: absolute;
  bottom: 0px;
  left: 50%;
  width: 180px;
  height: 3px;
  background: #111;
  transform: translateX(-50%);
}
section .title::after {
  position: absolute;
  bottom: -8px;
  left: 50%;
  font-size: 20px;
  color: crimson;
  padding: 0 5px;
  background: #fff;
  transform: translateX(-50%);
}

.home {
  display: flex;
  /* background-image: url("banner.jpg") no-repeat center; */
  height: 100vh;
  color: #fff;
  min-height: 500px;
  background-size: cover;
  background-attachment: fixed;
  font-family: "Ubuntu", sans-serif;
}

.home {
  .max-width {
    margin: auto 0 auto 30px;

    .home-content {
      > a {
        display: inline-block;
        background: crimson;
        color: #fff;
        font-size: 25px;
        padding: 12px 36px;
        margin-top: 20px;
        font-weight: 400;
        border-radius: 6px;
        border: 2px solid crimson;
        transition: all 0.3s ease;
      }

      > a:hover {
        color: crimson;
        background: none;
      }
      .text-1 {
        font-size: 27px;
      }

      .text-2 {
        font-size: 75px;
        font-weight: 600;
        margin-left: -3px;
      }

      .text-4 {
        font-size: 50px;
        font-weight: 600;
        margin-left: -3px;
      }
      .text-3 {
        font-size: 40px;
        margin: 5px 0;
        span {
          color: crimson;
          font-weight: 500;
        }
      }
    }
  }
}
</style>
