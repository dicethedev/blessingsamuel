<template>
  <header class="header" :class="{ 'scrolled-nav': scrolledNav }">
    <div class="overlay"></div>
    <nav>
      <div class="branding-logo">
        <a href="/#Home"><img src="@/assets/Logo.svg" alt="" /></a>
      </div>

      <ul v-show="!mobile" class="navigation">
        <li>
          <router-link class="nav-link" :to="{ name: '' }"
            ><span>01.</span>About</router-link
          >
        </li>

        <li>
          <!-- <a class="nav-link" href="/#experience" :to="{ name: '' }"
            ><span>02.</span>Experience</a
          > -->
          <router-link class="nav-link" :to="{ name: '' }"
            ><span>02.</span>Experience</router-link
          >
        </li>

        <li>
          <!-- <a class="nav-link" href="/#works" :to="{ name: '' }"
            ><span>03.</span>Work</a
          > -->
          <router-link class="nav-link" :to="{ name: '' }"
            ><span>03.</span>Work</router-link
          >
        </li>

        <li>
          <!-- <a class="nav-link" href="/#contact" :to="{ name: '' }"
            ><span>04.</span>Contact</a
          > -->
          <router-link class="nav-link" :to="{ name: '' }"
            ><span>04.</span>Contact</router-link
          >
        </li>

        <!-- Resume Button area is here -->
        <!-- href="/resume.pdf" -->
        <a class="resume-button" href="#" target="_blank">Resume</a>
      </ul>

      <!-- Nav Bar Icon when you switch to mobile -->
      <!-- Toogle Mobile Nav is click event for opening nav closing when you switch to mobile -->
      <!-- the icon-active is displaying when the mobileNav is true and the mobileNav will be trigger by toggleMobileNav -->
      <div class="icon">
        <img
          @click="toggleMobileNav"
          v-show="mobile"
          src="@/assets/Nav-bar.svg"
          :class="{ 'icon-active': mobileNav }"
        />
      </div>

      <!-- Animating the mobileNav here -->
      <!-- v-show id mobileNav is true here -->

      <transition name="mobileNav">
        <ul v-show="mobileNav" class="dropdown-nav">
          <!-- The Nav-close-bar and binded property is in this image area -->
          <img
            @click="toggleMobileNav"
            v-show="mobile"
            class="nav-close-bar"
            src="@/assets/Nav-close-bar.svg"
            :class="{ 'icon-active-2': mobileNav }"
          />

          <li>
            <a class="nav-link" href="/#about" :to="{ name: '' }"
              ><span>01.</span>About</a
            >
          </li>

          <li>
            <a class="nav-link" href="/#experience" :to="{ name: '' }"
              ><span>02.</span>Experience</a
            >
          </li>

          <li>
            <a class="nav-link" href="/#works" :to="{ name: '' }"
              ><span>03.</span>Work</a
            >
          </li>

          <li>
            <a class="nav-link" href="/#contact" :to="{ name: '' }"
              ><span>04.</span>Contact</a
            >
          </li>
          <!-- Resume Button area is here -->
          <!-- href="/resume.pdf" -->
          <a class="resume-link" href="#" target="_blank" rel="">Resume</a>
        </ul>
      </transition>
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
    transition: var(--transition);
    width: 90%;
    margin: 0 auto;
    // @media (min-width: 1140px) {
    //   max-width: 1140px;
    // }

    ul,
    .nav-link {
      font-weight: 400;
      color: var(--slate);
      list-style: none;
      text-decoration: none;
    }

    // The nav listing style here
    li {
      padding: 10px;
      margin-left: 10px;
    }

    .nav-link span {
      color: #00cffd;
      font-style: normal;
      font-weight: normal;
      //13px = 0.8125rem
      font-size: 0.875rem;
      margin-right: 0.325rem;
    }

    .nav-link {
      //17px = 1.0625rem
      font-size: 1rem;
      transition: var(--transition);
      padding-bottom: 4px;
      margin-right: 1.1625rem;

      &:hover {
        border: 1px dashed #00cffd;
        padding: 12px;
        border-radius: 0.625rem;
      }
    }

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
        margin-left: -5px !important;
      }

      img {
        // margin-left: 305px;
        width: 60px;
        height: 60px;
        transition: var(--transition);

        &:hover {
          border: 1px dashed #00cffd;
        }
      }
    }

    // The navigation is the class the name for all the nav link
    .navigation {
      display: flex;
      padding: 12px 0;
      justify-content: flex-end;
      align-items: center;
      margin-left: 32.0625rem;

      // @include breakpoint-up(medium) {
      //   margin-left: 600px;
      // }
    }

    .resume-button {
      position: relative;
      display: inline-block;
      cursor: pointer;
      font-size: 16px;
      font-weight: 400;
      //60px = 3.75rem
      margin-left: 2.75rem;
      color: #00cffd;
      background-color: transparent;
      border: 2px solid;
      border-color: #00cffd #00e9df;
      //10px = 0.625rem;
      border-radius: 0.625rem;
      line-height: 1;
      //18px  1.125rem 40px = 2.5rem
      padding: 1rem 2.5rem;
      text-decoration: none;
      transition: var(--transition);
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
        transition: opacity 150ms ease-in-out;
      }

      &:hover::before {
        opacity: 1;
      }
    }

    // Nav-bar styling is here
    .icon {
      display: flex;
      align-items: center;
      position: absolute;
      top: 0;
      right: 24px;
      height: 100%;

      // Nav-bar hamburger styling is here
      img {
        top: 2.4375rem;
        cursor: pointer;
        width: 2.5rem;
        height: 1.5rem;
        transition: 0.8s ease all;

        &:hover {
          border: 1px dashed #00cffd;
          padding: 9px;
          //10px = 0.625rem
          border-radius: 0.625rem;
        }
      }
    }

    // Nav-bar animating to rotate to Nav-close-bar
    .icon-active {
      transform: rotateX(180deg);
      transition: 100ms var(--transition);
    }

    // The dropdown menu when you click on Nav-bar on mobile
    .dropdown-nav {
      position: fixed;
      display: flex;
      justify-content: center;
      flex-direction: column;
      width: 100vw;
      max-width: 21.1875rem;
      height: 100%;
      right: 0;
      margin: 0;
      outline: 0;
      z-index: 1;
      background-color: #16294b;
      transform: translate(0vw);
      transition: var(--transition);

      // Nav-close-bar hamburger styling is here
      img {
        position: absolute;
        cursor: pointer;
        top: 1.5rem;
        margin-left: 17.1875rem;
        margin-right: 3rem;
        width: 1.25rem;
        height: 1.875rem;
        // padding-top: -5%;
        transition: transform 100ms var(--transition);

        &:hover {
          border: 1px dashed #00cffd;
          padding: 9px;
          //10px = 0.625rem
          border-radius: 0.625rem;
        }
      }

      li {
        .nav-link {
          position: absolute;
          display: flex;
          justify-content: center;
          align-items: center;
          // flex-direction: row;
          text-decoration: none;
          color: #fff;
          //18px = 1.125rem
          font-size: 1.125rem;
          text-align: center;
        }

        .nav-link {
          //117px = 7.1875rem
          margin-left: 7.1875rem;
        }

        .nav-link span {
          //14px // 10px = 0.625rem
          margin-right: 0.625rem;
          font-size: 0.875rem;
          font-weight: 200;
        }
      }
    }
    .resume-link {
      cursor: pointer;
      margin-left: 6.1875rem;
      margin-right: 5.125rem;
      //80px = 5rem
      margin-top: 5rem;
      color: #00cffd;
      background-color: transparent;
      font-size: 16px;
      width: max-content;
      border: 1px solid #00cffd;
      border-radius: 0.625rem;
      line-height: 1;
      //10px = 0.625rem
      padding: 1.125rem 3.125rem;
      text-decoration: none;
      transition: var(--transition);

      &:hover {
        color: #fff;
        background-color: rgba(13, 186, 255, 0.185);
        transition: transform 100ms var(--transition);
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