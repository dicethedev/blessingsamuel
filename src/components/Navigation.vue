<template>
  <header class="header" :class="{ 'scrolled-nav': scrolledNav }">
    <nav class="nav">
      <ul>
        <li>
          <a href="/"><img class="my-logo  animate__animated animate__backInDown" src="@/assets/Logo.svg" alt="" /></a>
        </li>
        <li>
          <a class="resume-button" href="./resume.pdf" target="_blank"
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

<style lang="scss">
@import "/src/scss/_mixins.scss";

.header {
  background-color: var(--color-bg);
  width: 100%;
  position: fixed;
  transition: var(--transition);
  color: #fff;
  z-index: 3;
  overflow: hidden;

  .nav {
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
        border: 1px dashed var(--color-primary);
        border-radius: 10px;
      }
    }

    .resume-button {
      position: relative;
      cursor: pointer;
      font-size: 12px;
      color: var(--color-primary);
      background-color: transparent;
      border: 1px solid;
      border-color: var(--color-primary);
      //   border-image: linear-gradient(45deg, red , yellow);
      //  border-image-slice: 1;
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
        background-color: var(--color-primary-variant);
        border-radius: 15px 0px 15px 0px;
        opacity: 0;
        transition: opacity 200ms ease-in-out;
        transition: var(--transition);
      }

      &:hover::before {
        opacity: 2;
      }
    }
  }
}

// The scrolled-nav class area style is here
.scrolled-nav {
  background-color: var(--color-bg);
  box-shadow: 0px 2px 10px var(--color-primary);
  -webkit-box-align: center;
  height: 110px;

  nav {
    padding: 8px 0;

    .branding-logo {
      img {
        width: 65px;
        height: 65px;
      }
    }
    // .resume-button {
    //   // margin-top: -0.2rem;
    // }
  }
}
</style>