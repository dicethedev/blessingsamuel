<template>
  <div class="home">
    <section class="home-content">
      <div class="hero-text container">
        <h1>Hi, my name is</h1>

        <div class="big-heading-1">
          <h2>Blessing Samuel.</h2>
        </div>

        <!-- animate__pulse animate__infinite -->
        <h3
          class="
            big-heading-2
            animate__animated animate__pulse animate__infinite
          "
        >
          The Tech guy with the Web.
        </h3>

        <div class="small-heading-detail">
          <p>
            I love to build and style things that live on the web with great
            user interface & experience. I am very good with HTML5, CSS3 (SCSS
            included). I am also very good with JavaScript and its frameworks
            such as Vue & React. I have over 1 years professional experience in
            front end development.
            <!-- <a href="https://myshelta.com/" target="_blank" rel="norefer">
              Shelta.
            </a> -->
          </p>
        </div>

        <!-- See projects is here -->
        <!--  <a v-bind:href="`mailto:${email}`">See Projects</a> -->
        <div class="home-link">
          <a href="#project">See Projects</a>
          <div class="water-liquid"></div>
        </div>
      </div>
    </section>
    <div class="link-to-left">
      <ul class="style-left">
        <!-- Github link -->
        <li>
          <a
            href="https://github.com/dicethedev"
            target="_blank"
            rel="noreferrer"
          >
            <img src="@/assets/github.svg" alt="" />
          </a>
        </li>
        <!-- Twitter link -->
        <li>
          <a
            href="https://twitter.com/dicethedev"
            target="_blank"
            rel="noreferrer"
          >
            <img src="@/assets/twitter.svg" alt="" />
          </a>
        </li>
        <!-- Instagram link -->
        <li>
          <a href="#" target="_blank" rel="noreferrer">
            <img src="@/assets/instagram-fill.svg" alt="" />
          </a>
        </li>
        <!-- Linkedin link -->
        <li>
          <a
            href="https://www.linkedin.com/in/blessing-samuel-6a72b1211/"
            target="_blank"
            rel="noreferrer"
          >
            <img src="@/assets/linkedin.svg" alt="" />
          </a>
        </li>
        <!-- Line-focus bottom is here -->
        <img class="line-focus" src="@/assets/line-focus.svg" alt="" />
      </ul>
    </div>

    <div>
      <About />
    </div>

    <div>
      <Experience />
    </div>

    <div>
      <Project />
    </div>

    <div>
      <SkillSet />
    </div>

    <div>
      <Contact />
    </div>
    <router-view />
  </div>
</template>

<script>
// @ is an alias to /src
import Contact from "@/views/Contact.vue";
import SkillSet from "@/views/SkillSet.vue";
import Project from "@/views/Project.vue";
import Experience from "@/views/Experience.vue";
import About from "@/views/About.vue";
export default {
  name: "Home",
  data() {
    return {
      show: true,
      email: "dicethedev@gmail.com",
    };
  },
  components: {
    About,
    Experience,
    Project,
    SkillSet,
    Contact,
  },

  methods: {},
};
</script>

<style lang="scss">
// import _mixings.scss file here
@import "/src/scss/_mixins.scss";

:root {
  --color-focus: #00cffd;
  --fz-sm: 13px;
  --fz-md: 18px;
  --fz-heading: 32px;
  --lightest-slate: #ccd6f6;
  --light-slate: #e6f1ff;
  --darkest-slate: #8892b0;
  --easing: cubic-bezier(0.645, 0.045, 0.355, 1);
  --animate-duration: 0.1ms;
  --animate-delay: 400ms;
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

.home-content {
  width: 100%;
  padding: 84px 6.944vw 0;
  position: relative;
  min-height: 711px;
  display: flex;
  align-items: center;
  // margin-top: -5.75rem;
  // margin-left: -180px;

  //Mobile Responsiveness
  @include breakpoint-down(small) {
    margin-top: -3rem;
    margin-left: -1.5rem;
  }

  //Mobile Responsiveness
  @include breakpoint-down(medium) {
    margin-top: -3rem;
    margin-left: -10px;
  }

  .hero-text {
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    margin-top: 90px;

    h1 {
      margin: 0px 0px 30px 4px;
      color: #00cffd;
      //5px = 0.3125rem
      word-spacing: 0.3125rem;
      margin-bottom: 1rem;
      font-size: clamp(13px, 5vw, 18px);
      font-weight: 400;
    }

    .big-heading-1 {
      margin: 0px;
      h2 {
        //50px = 3.125rem
        font-size: clamp(40px, 6vw, 70px);
        color: var(--lightest-slate);
        margin-bottom: 1rem;
      }
    }

    h3 {
      font-size: clamp(40px, 6vw, 62px);
      margin-bottom: 1rem;
      color: var(--darkest-slate);

      .big-heading-2 {
        margin: 0px;
        line-height: 0.9;
      }
    }

    .small-heading-detail {
      margin: 15px 0px 0px;
      max-width: 520px;
      color: var(--darkest-slate);

      p {
        margin: 0px 0px 15px;
        line-height: 1.5;
        //16px
        font-size: 1rem;
      }

      p:last-child,
      p:last-of-type {
        margin: 0px;
      }
    }

    .home-link {
      //70px = 4.375rem
      margin-top: 4.375rem;

      a {
        padding: 15px 25px;
        border: unset;
        border-radius: 0 20px;
        text-decoration: none;
        background: var(--color-focus);
        position: relative;
        color: var(--light-slate);
        letter-spacing: 5px;
        text-transform: uppercase;
        word-spacing: 5px;
        font-weight: 400;
        transition: all 250ms ease-in-out;
        overflow: hidden;

        &::before {
          content: "";
          position: absolute;
          top: 0;
          left: 0;
          height: 100%;
          width: 0;
          border-radius: 0 20px;
          background-color: var(--light-slate);
          transition: all 250ms ease-in-out;
        }

        &:hover {
          color: #e8e8e8;
        }

        &:hover::before {
          width: 90%;
        }
      }
    }
  }
}

.link-to-left {
  width: 40px;
  position: fixed;
  bottom: 0px;
  left: 40px;
  right: auto;
  z-index: 10;
  transition: var(--transition);

  ul,
  .style-left {
    display: flex;
    flex-direction: column;
    -webkit-box-align: center;
    align-items: center;
    margin: 0px;
    padding: 0px;
    list-style: none;
    margin-top: -350px;
    margin-right: -20px;
  }

  li {
    display: list-item;
    text-align: -webkit-match-parent;
    // margin-top: -300px;
  }
  li a {
    padding: 10px;
  }

  a {
    display: inline-block;
    text-decoration: none;
    text-decoration-skip-ink: auto;
    color: inherit;
    position: relative;
    transition: var(--transition);
  }

  li a img {
    width: 23px;
    height: 23px;
    transition: var(--transition);
    animation-delay: var(--easing);

    &:hover {
      border: 1px dashed #00cffd;
      padding: 5px;
      border-radius: 8px;
    }
  }
  // Line-focus styling area is here
  .line-focus {
    width: 1.8px;
    position: fixed;
    bottom: 0px;
    right: auto;
    z-index: 10;

    img {
      margin-right: -35px;
    }
  }
  //Mobile Responsiveness
  @include breakpoint-down(small) {
    display: none;
  }

  //Mobile Responsiveness
  @include breakpoint-down(medium) {
    display: none;
  }

  //Responsiveness for Desktop or Laptop
  @include breakpoint-down(large) {
    margin-left: -25px;
  }
}

//link-to-right styling area
// .link-to-right {
//   display: flex;
//   flex-direction: column;
//   -webkit-box-align: center;
//   align-items: center;
//   position: fixed;
//   margin-left: 2rem;

//   a {
//     display: inline-block;
//     margin: 20px auto;
//     padding: 10px;
//     margin-left: 120px;
//     margin-top: -205px;
//     font-size: 12px;
//     font-weight: 400;
//     line-height: 18px;
//     letter-spacing: 0.1em;
//     -webkit-writing-mode: vertical-rl;
//     writing-mode: vertical-rl;
//     text-decoration: none;
//     text-decoration-skip-ink: auto;
//     color: #8892b0;
//     transition: var(--transition);

//     &:hover {
//       border: 1px dashed #00cffd;
//       color: #00cffd;
//     }
//   }

//   ul,
//   .style-right {
//     // display: flex;
//     flex-direction: column;
//     -webkit-box-align: center;
//     align-items: center;
//     margin: 0px;
//     padding: 0px;
//     list-style: none;
//     margin-top: 200px;
//     // Margining it to right is right here
//     margin-left: 120px;
//   }

//   // focus-line styling area is here
//   .focus-line {
//     width: 1.8px;
//     position: fixed;
//     bottom: 0px;
//     right: auto;
//     z-index: 10;
//   }
//   //Mobile Responsiveness
//   @include breakpoint-down(small) {
//     display: none;
//   }
//   //Responsiveness for Desktop or Laptop
//   @include breakpoint-down(medium) {
//     display: none;
//   }

//   //Responsiveness for Desktop or Laptop
//   @include breakpoint-down(large) {
//     display: none;
//   }
// }
</style>