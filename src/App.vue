<template>
  <!-- Preloader for the page is here -->
  <Loader />
  <div class="app">
    <Navbar />
    <router-view />
  </div>
</template>

<script>
import Loader from "@/components/Loader.vue";
import Navbar from "@/components/Navbar.vue";
export default {
  name: "App",
  components: {
    Navbar,
    Loader,
  },
};
</script>


<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Rubik:wght@300;400;500;600&display=swap");

:root {
  --color-bg: #1f1f38;
  --color-bg-variant: #2c2c6c;
  --color-loader: #22224e;
  --color-primary: #4ca5ff;
  --color-linear-gradient: linear-gradient(90deg,#4ca5ff 2.34%,#b673f8 100.78%); 
  --color-primary-variant: rgba(77, 181, 255, 0.4);
  --color-secondary: #b673f8;
  --color-focus: #00cffd;
  --fz-sm: 13px;
  --fz-md: 16px;
  --fz-lg: 18px;
  --fz-heading: 32px;
  --normal-slate: #a8b2d1;
  --lightest-slate: #ccd6f6;
  --light-slate: #e6f1ff;
  --darkest-slate: #8892b0;
  
     ---container-width-lg: 75%;
     ---container-width-md: 86%;
     ---container-width-sm: 90%; 
     ---transition: all 400ms ease-out;
  --transition: all 0.25s cubic-bezier(0.645, 0.045, 0.355, 1);
  --easing: cubic-bezier(0.645, 0.045, 0.355, 1);
  --animate-duration: 0.4ms;
  --animate-delay: 400ms;
}

*,
::before,
::after {
  padding: 0;
  margin: 0;
  margin-top: 0px;
  margin-right: 0px;
  box-sizing: border-box;
  font-family: "Rubik", sans-serif;
}


html {
     scroll-behavior: smooth;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  margin: 0px 0px 10px;
  font-weight: 600;
  color: #fff;
  line-height: 1.1;
}


.app {
  background-color: var(--color-bg);
  position: relative;
  min-height: 300vh;
  // // overflow-x: hidden;
  // // flex-direction: column;
  // @media (min-width: 900px) {
  //   flex-direction: column !important;
  // }

  // .app-content {
  //   padding: 0 20px;
  //   flex: 1;
  //   position: relative;
  // }
}

// Scrollbar customize style is here
body::-webkit-scrollbar {
   width: 6px;
}

body::-webkit-scrollbar-thumb {
  border-radius: 10px;
  border: 3px solid var(--app-color);
  background-color: var(--normal-slate);
}

body::-webkit-scrollbar-track {
  background: var(--color-bg);
}

::selection {
  background-color: var(--lightest-navy);
  color: var(--lightest-slate);
}



// utility classes

.flex {
  display: flex;
}

.flex-column {
  flex-direction: column;
}

// .container {
//   width: 100%;
//   padding: 40px 10px;
//   max-width: 850px;
//   margin: 0 auto;

//   // @media (min-width: 900px) {
//   //   padding-top: 72px;
//   // }
// }

.container {
     /* 75% */
     width: var( ---container-width-lg);
     margin: auto;
}


/* Media Queries (Medium Devices) */
@media screen and (max-width: 1024px) {
     .container {
          /* 86% */
          width: var(---container-width-md);
     }

    
}

/* Media Queries (Small Devices) */
@media screen and (max-width: 600px) {
     .container {
          /* 90% */
          width: var(---container-width-sm);
     }

    // section {
    //       margin-top: 4rem;
    //  }
}

</style>

