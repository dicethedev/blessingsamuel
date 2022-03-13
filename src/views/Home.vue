<template>
  <div class="home">
    <section class="home-title">
      <div class="hero-text container">
        <h1>Hi, my name is</h1>

        <!-- <hr /> -->
        <div class="big-heading">
          <h2>Blessing Samuel.</h2>
        </div>

        <div class="big-heading-2">
          <!-- <h3>The full stop to your search.</h3> -->
          <!-- <h3>I design things for the web.</h3> -->
          <h3>The Tech guy with the Web.</h3>
          <!-- <hr /> -->
        </div>
        <div class="small-heading-detail">
          <p>
            I love to build and style things that live on web pages with great
            user interface & experience. I am very good with HTML5, CSS3 (SCSS
            included). I am also very good with JavaScript and its frameworks
            such as Vuejs & Angular. I have over 2 years professional experience
            in front end development.
            <!-- <a href="https://myshelta.com/" target="_blank" rel="norefer">
              Shelta.
            </a> -->
          </p>
        </div>

        <!-- See projects is here -->
        <!--  <a v-bind:href="`mailto:${email}`">See Projects</a> -->
        <div class="action-button">
          <a href="#" target="_blank" rel="noreferrer">See Projects</a>
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
    <!-- 
    <div class="link-to-right">
      <a v-bind:href="`mailto:${email}`">dicethedev@gmail.com</a> -->

    <!-- <ul class="style-right"> -->
    <!-- Line-focus bottom is here -->
    <!-- <img class="focus-line" src="@/assets/focus-line.svg" alt="" /> -->
    <!-- </ul>
    </div> -->

    <section class="flex">
      <About />
    </section>

    <section class="flex">
      <Project />
    </section>

    <section class="flex">
      <Experience />
    </section>

    <section class="flex">
      <Skills />
    </section>
  </div>
</template>

<script>
// @ is an alias to /src
import Skills from "@/views/Skills.vue";
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
    Skills,
  },
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
  --easing: cubic-bezier(0.645, 0.045, 0.355, 1);
  --transition: all 0.25s cubic-bezier(0.645, 0.045, 0.355, 1);
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

.home-title {
  position: relative;
  height: 100vh;
  margin-top: -5.75rem;
  margin-left: 2rem;

  //Mobile Responsiveness
  @include breakpoint-down(medium) {
    margin-top: -2rem;
  }

  .hero-text {
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    color: #ccd6f6;

    h1 {
      margin: 0px 0px 30px 4px;
      color: #00cffd;
      //5px = 0.3125rem
      word-spacing: 0.3125rem;
      margin-bottom: 1rem;
      font-size: clamp(var(--fz-sm), 5vw, var(--fz-md));
      font-weight: 400;
      transition: var(--transition);
      transition-delay: 100ms;

      //Responsiveness for Desktop or Laptop
      @include breakpoint-down(large) {
        margin-left: 20px;
      }
    }

    .big-heading {
      margin: 0px;
      h2 {
        //50px = 3.125rem
        font-size: 3.125rem;
        color: #ccd6f6;
        margin-bottom: 1rem;

        //Mobile Responsiveness
        @include breakpoint-down(medium) {
          //20px = 1.25rem
          font-size: 2rem;
        }

        //Responsiveness for Desktop or Laptop
        @include breakpoint-down(large) {
          margin-left: 15px;
        }
      }
    }

    .big-heading-2 {
      margin: 0px;
      h3 {
        font-size: 60px;
        margin-bottom: 1rem;
        color: #8892b0;
        line-height: 0.9;

        //Mobile Responsiveness
        @include breakpoint-down(medium) {
          //35px = 2.1875rem
          font-size: 2.1875rem;
          word-break: break-word;
        }

        //Responsiveness for Desktop or Laptop
        @include breakpoint-down(large) {
          margin-left: 15px;
        }
      }
    }

    .small-heading-detail {
      margin: 15px 0px 0px;
      max-width: 520px;
      color: #8892b0;

      //Responsiveness for Desktop or Laptop
      @include breakpoint-down(large) {
        margin-left: 20px;
      }

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

    .action-button {
      //70px = 4.375rem
      margin-top: 4.375rem;

      a {
        color: var(--color-focus);
        background-color: transparent;
        border: 1px solid var(--color-focus);
        border-radius: 30px 0px 30px 0px;
        padding: 1.25rem 3rem;
        word-spacing: 5px;
        font-size: 1rem;
        line-height: 1;
        text-decoration: none;
        cursor: pointer;
        overflow: hidden;

        //Responsiveness for Desktop or Laptop
        @include breakpoint-down(large) {
          margin-left: 30px;
        }

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
  margin-left: 5rem;

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
    width: 25.5px;
    height: 25.5px;
    transition: var(--transition);
    // transition: var(--easing);

    &:hover {
      border: 1px dashed #00cffd;
      padding: 10px;
      border-radius: 20px;
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
  //Responsiveness for Desktop or Laptop
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