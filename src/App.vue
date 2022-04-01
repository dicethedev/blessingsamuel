<template>
  <div class="app flex flex-column">
    <Navigation />
    <div></div>
    <router-view />
  </div>
</template>

<script>
import Navigation from "@/components/Navigation.vue";
export default {
  name: "App",
  components: {
    Navigation,
  },
};
</script>


<style lang="scss">
//Use SCSS framework for CSS
@import url("https://fonts.googleapis.com/css2?family=Rubik:wght@300;400;500;600&display=swap");

*,
::before,
::after {
  margin: 0;
  padding: 0;
  // box-sizing: border-box;
  box-sizing: border-box;
  font-family: "Rubik", sans-serif;
}

.app {
  background-color: #112240;
  position: relative;
  min-height: 730vh;
  // overflow-x: hidden;
  // flex-direction: column;
  @media (min-width: 900px) {
    flex-direction: column !important;
  }

  // .app-content {
  //   padding: 0 20px;
  //   flex: 1;
  //   position: relative;
  // }
}
// Scrollbar customize style is here
::-webkit-scrollbar {
  width: 5px;
  background-color: #112240;
}

::-webkit-scrollbar-track {
  border-radius: 5px;
  // box-shadow: inset 0 0 10px rgba(0, 0, 0, 0.25);
}

::-webkit-scrollbar-thumb {
  border-radius: 50px;
  background-color: #8892b0;
}

// ::-webkit-scrollbar-thumb:hover {
//   background-color: #00cffd;
// }

// utility classes

.flex {
  display: flex;
}

.flex-column {
  flex-direction: column;
}

.container {
  width: 90%;
  padding: 40px 10px;
  max-width: 850px;
  margin: 0 auto;

  @media (min-width: 900px) {
    padding-top: 72px;
  }
}
</style>

