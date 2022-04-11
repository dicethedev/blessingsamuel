<template>
  <header class="header" :class="{ 'scrolled-nav': scrolledNav }">
    <nav class="nav">
      <ul>
        <li>
          <a href="/"><img class="my-logo" src="@/assets/Logo.svg" alt="" /></a>
        </li>
        <li>
          <a class="resume-button" href="./profile.pdf" target="_blank"
            >Resume</a
          >
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: "navigation",
  data() {
    return {
      scrolledNav: null,
      // mobile: null,
      // mobileNav: null,
      // windowWidth: null,
    };
  },
  // created() {
  //   window.addEventListener("resize", this.checkScreen);
  //   this.checkScreen();
  // },

  //this mounted is for scrollNav function
  mounted() {
    window.addEventListener("scroll", this.updateScroll);
  },

  methods: {
    // readPdf() {
    //   const pdf = "./profile.pdf";
    //   window.open(require(pdf), "_blank");
    // },

    // toggleMobileNav() {
    //   this.mobileNav = !this.mobileNav;
    // },

    updateScroll() {
      const scrollPosition = window.scrollY;
      if (scrollPosition > 50) {
        this.scrolledNav = true;
        return;
      }
      this.scrolledNav = false;
    },

    // This functionality is remove for now. It will be added later in the future
    // checkScreen() {
    //   this.windowWidth = window.innerWidth;
    //   if (this.windowWidth <= 700) {
    //     this.mobile = true;
    //     return;
    //   }
    //   //If this is not true return false -- that is the statement below
    //   this.mobile = false;
    //   this.mobileNav = false;
    //   return;
    //   //after this -- I created a lifecycle hook above called created
    // },
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
  z-index: 1;
  background-color: #112240;
  width: 100%;
  position: fixed;
  transition: var(--transition);
  color: #fff;
  overflow: hidden;

  .nav {
    // position: fixed;
    z-index: 10;
    width: 100%;
    left: 0;
    top: 0;
    padding: 20px 6.994vw;

    @media (max-width: 575.98px) {
      width: 100%;
      padding: 16px 25px 16px 27px;
    }

    ul {
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    li {
      list-style: none;
    }

    // My Logo styling is here
    .my-logo {
      width: 75px;
      height: 75px;
      transition: 200ms ease-in-out;
      transition: var(--transition);

      &:hover {
        border: 1px dashed #00cffd;
        border-radius: 10px;
      }
    }

    .resume-button {
      position: relative;
      cursor: pointer;
      font-size: 12px;
      color: #00cffd;
      background-color: transparent;
      border: 1px solid;
      border-color: #00cffd #00e9df;
      border-radius: 15px 0px 15px 0px;
      text-decoration: none;
      padding: 0.5rem 2rem;
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

// The scrolled-nav class area style is here
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
      margin-top: -0.2rem;
    }
  }
}
</style>