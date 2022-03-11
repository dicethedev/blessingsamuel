<template>
  <header class="header" :class="{ 'scrolled-nav': scrolledNav }">
    <div class="overlay"></div>
    <nav>
      <div class="branding-logo">
        <a href="/#Home"><img src="@/assets/Logo.svg" alt="" /></a>
      </div>

      <div>
        <!-- Resume Button area is here -->
        <!-- href="/resume.pdf" -->
        <a class="resume-button" href="#" target="_blank">Resume</a>
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

  mounted() {
    window.addEventListener("scroll", this.updateScroll);
  },

  methods: {
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

  .overlay {
    opacity: 0;
    position: fixed;
    top: 0;
    right: 0;
    left: 0;
    bottom: 0;
    background-image: linear-gradient(var(--light-slate), transparent);
  }

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
      // margin-top: 1rem;
      // margin-left: 2rem;
      // margin-bottom: 1rem;

      @media (max-width: 640px) {
        margin-left: 5px !important;
      }

      img {
        // margin-left: 305px;
        width: 60px;
        height: 60px;
        transition: 200ms ease-in-out;

        &:hover {
          border: 1px dashed #00cffd;
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
      border-radius: 20px 0px 20px 0px;
      text-decoration: none;
      //10px = 0.625rem;
      line-height: 1;
      //18px  1.125rem 40px = 2.5rem
      padding: 1rem 2rem;
      margin: 1rem 2rem 1rem;
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

  nav {
    padding: 8px 0;

    .branding-logo {
      img {
        width: 65px;
        height: 65px;
      }
    }
  }
}
</style>