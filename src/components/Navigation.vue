<template>
  <header class="header" :class="{ 'scrolled-nav': scrolledNav }">
    <nav>
      <div class="branding-logo">
        <a href="/" aria-label="home"><img src="@/assets/Logo.svg" alt="" /></a>
      </div>

      <!-- Resume Button area is here -->
      <div>
        <!-- href="/resume.pdf"  @click="readPdf" -->
        <a class="resume-button" href="./profile.pdf" target="_blank">Resume</a>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: "navigation",
  data() {
    return {
      scrolledNav: null,
      mobile: null,
      mobileNav: null,
      windowWidth: null,
    };
  },
  created() {
    window.addEventListener("resize", this.checkScreen);
    this.checkScreen();
  },

  //this mounted is for scrollNav function
  mounted() {
    window.addEventListener("scroll", this.updateScroll);
  },

  methods: {
    // readPdf() {
    //   const pdf = "./profile.pdf";
    //   window.open(require(pdf), "_blank");
    // },

    toggleMobileNav() {
      this.mobileNav = !this.mobileNav;
    },

    updateScroll() {
      const scrollPosition = window.scrollY;
      if (scrollPosition > 50) {
        this.scrolledNav = true;
        return;
      }
      this.scrolledNav = false;
    },

    checkScreen() {
      this.windowWidth = window.innerWidth;
      if (this.windowWidth <= 640) {
        this.mobile = true;
        return;
      }
      //If this is not true return false -- that is the statement below
      this.mobile = false;
      this.mobileNav = false;
      return;
      //after this -- I created a lifecycle hook above called created
    },
  },
};
</script>

<style lang="scss" scoped>
@import "/src/scss/_mixins.scss";

//  The root contain what i declare and I will like to use it later
:root {
  --dark-slate: #495670;
  --slate: #8892b0;
  --light-slate: #a8b2d1;
  --lightest-slate: #ccd6f6;
  --white: #e6f1ff;
  --easing: cubic-bezier(0.645, 0.045, 0.355, 1);
  --transition: all 0.25s cubic-bezier(0.645, 0.045, 0.355, 1);
}

.header {
  position: relative;
  z-index: 1;
  background-color: #112240;
  width: 100%;
  position: fixed;
  transition: var(--transition);
  color: #fff;
  overflow: hidden;

  nav {
    position: relative;
    display: flex;
    flex-direction: row;
    width: 90%;
    margin: 0 auto;
    justify-content: space-between;

    // My Logo styling is here

    .branding-logo {
      display: flex;
      align-items: center;
      width: 3.75rem;
      height: 3.75rem;
      margin: 1rem 2rem 1rem;

      @media (max-width: 640px) {
        margin-left: 5px !important;
      }

      //Responsiveness for Desktop or Laptop
      @include breakpoint-down(large) {
        margin-left: -15px;
      }

      img {
        // margin-left: 305px;
        width: 60px;
        height: 60px;
        transition: 200ms ease-in-out;
        transition: var(--transition);

        &:hover {
          border: 1px dashed #00cffd;
          border-radius: 10px;
        }
      }
    }

    .resume-button {
      position: relative;
      display: inline-block;
      justify-content: flex-end;
      cursor: pointer;
      font-size: 14px;
      font-weight: 400;
      //60px = 3.75rem
      color: #00cffd;
      background-color: transparent;
      border: 1px solid;
      border-color: #00cffd #00e9df;
      border-radius: 15px 0px 15px 0px;
      text-decoration: none;
      //10px = 0.625rem;
      //18px  1.125rem 40px = 2.5rem
      padding: 0.5rem 2rem;
      // margin: 1rem 2rem 1rem;
      margin-top: 2rem;
      margin-right: 20px !important;
      overflow: hidden;

      &::before {
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        bottom: 0;
        right: 0;
        background-color: rgba(13, 186, 255, 0.185);
        opacity: 0;
        transition: opacity 200ms ease-in-out;
      }

      &:hover::before {
        opacity: 2;
      }
    }
  }
}

// The scrolled nav class area style is here
.scrolled-nav {
  background-color: #112240;
  box-shadow: 0px 5px 10px #12284e;
  -webkit-box-align: center;
  height: 100px;

  nav {
    padding: 8px 0;

    .branding-logo {
      img {
        width: 65px;
        height: 65px;
      }
    }
    .resume-button {
      margin-top: 1.4rem;
    }
  }
}
</style>