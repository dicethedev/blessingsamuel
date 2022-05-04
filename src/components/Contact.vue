<template>
  <!-- This area consist of both contact and footer section -->
  <div
    class="
      container
      button-style-1
      animate__animated animate__bounce animate__infinite
    "
  >
    <h2 class="heading-numbering">
      <span>05.</span> What’s Next?
      <div class="button-style-2"></div>
    </h2>
  </div>
  <div class="contact-me" id="contact-me">
    <h2>Get me Hired!</h2>
    <p class="container">
      I'm currently looking for any new opportunities, my inbox is always open. If you’re
      currently have a role for Blessing, please don’t hestiate to get in touch
      with me. I’ll try my best to get back to you on time! Thank you!
    </p>
    <button class="email-link">
      <a :href="`mailto:${email}`">Say Hello to Blessing</a>
    </button>
  </div>

  <footer class="footer-area">
    <!-- Social link available on Mobile device -->
    <div class="social-link">
      <ul>
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
      </ul>
    </div>

    <div class="design-build-destination">
      <h3>Designed & Built by Blessing Samuel</h3>
      <!-- Figma Destination -->
      <a
        href="https://www.figma.com/file/FrJ9xgmbpnefZUTFBr0CNE/Blessing-Samuel-Portfolio?node-id=0%3A1"
        target="_blank"
        rel="noreferrer"
        ><img src="../assets/fa-brands_figma.svg" alt="figma"
      /></a>
      <!-- Github Destination -->
      <a href="https://github.com/dicethedev/blessingsamuel"
        ><img src="../assets/akar-icons_link-out.svg" alt=""
      /></a>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Contact",
  data() {
    return {
      email: "dicethedev@gmail.com",
    };
  },
};
</script>

<style lang="scss" scoped>
@import "/src/scss/_mixins.scss";
:root {
  --color-bg: #1f1f38;
  --color-bg-variant: #2c2c6c;
  --color-loader: #22224e;
  --color-primary: #4db5ff;
  --color-primary-variant: rgba(77, 181, 255, 0.4);
  --color-focus: #00cffd;
  --fz-sm: 13px;
  --fz-md: 16px;
  --fz-lg: 18px;
  --fz-heading: 32px;
  --normal-slate: #a8b2d1;
  --lightest-slate: #ccd6f6;
  --light-slate: #e6f1ff;
  --darkest-slate: #8892b0;
}

.button-style-1 {
  background-color: transparent;
  border: 1px dashed var(--color-primary);
  border-radius: 0px 20px;
  padding: 1.25rem 1.88rem;
  word-spacing: 5px;
  width: 275px;
  height: 60px;
  line-height: 1;
  text-decoration: none;
  margin-top: 100px;

  //Mobile Responsiveness
  @include breakpoint-down(medium) {
    width: 220px;
    height: 50px;
  }

  .heading-numbering > h2 {
    position: relative;
    margin: 10px 0px 40px;
    width: 100%;
    font-size: clamp(26px, 5vw, var(--fz-heading));
    white-space: nowrap;
  }

  h2 {
    font-size: 25px;
    font-weight: 700;
    color: var(--light-slate);

    //Mobile Responsiveness
    @include breakpoint-down(small) {
      font-size: 17px;
    }
    //Mobile Responsiveness
    @include breakpoint-down(medium) {
      font-size: 18px;
    }
    span {
      color: var(--color-primary);
      font-size: 19px;
      font-weight: 200;
      margin-right: 2px;

      //Mobile Responsiveness
      @include breakpoint-down(small) {
        font-size: 16px;
      }

      //Mobile Responsiveness
      @include breakpoint-down(medium) {
        font-size: 17px;
      }
    }
    .button-style-2 {
      background-color: var(--color-primary);
      border-radius: 0px 20px;
      padding: 1.25rem 1.88rem;
      width: 122px;
      height: 61px;
      cursor: pointer;
      margin-top: -49px;
      margin-left: 123px;

      //Mobile Responsiveness
      @include breakpoint-down(medium) {
        width: 90px;
        height: 50px;
        margin-top: -41px;
        margin-left: 100px;
      }
    }
  }
}

.contact-me {
    max-width: 600px;
    margin: 0px auto 100px;
    text-align: center;
    margin-top: 70px;

  h2 {
    font-size: clamp(40px, 5vw, 60px);
    font-style: italic;
    color: var(--lightest-slate);
  }

  p {
    color: var(--darkest-slate);
    font-size: var(--fz-md);
    font-weight: 200;
    line-height: 26.44px;
    margin-top: 20px;

    p:last-child,
    p:last-of-type {
      margin: 0px;
    }

    @media (max-width: 480px) {
      font-size: 14px;
    }
  }

  .email-link {
    text-align: center;
    font-size: 16px;
    font-weight: 300;
    word-spacing: 5px;
    background-color: transparent;
    border: 1px solid var(--color-primary-variant);
    border-radius: 10px;
    padding: 1.25rem 1.75rem;
    width: fit-content;
    margin-top: 50px;
    cursor: pointer;

    a {
      display: inline-block;
      text-decoration: none;
      text-decoration-skip-ink: auto;
      position: relative;
      color: var(--color-primary);
    }
  }
}

.footer-area {
  display: flex;
  -moz-box-pack: center;
  justify-content: center;
  -moz-box-align: center;
  align-items: center;
  flex-direction: column;
  height: auto;
  min-height: 70px;
  padding: 15px;
  text-align: center;

  .social-link {
    display: none;

    @media (max-width: 768px) {
      display: block;
      width: 100%;
      max-width: 270px;
      margin: 0px auto 10px;
      color: var(--lightest-slate);
    }

    ul {
      display: flex;
      -moz-box-pack: justify;
      justify-content: space-between;
      -moz-box-align: center;
      align-items: center;
      padding: 0px;
      margin: 0px;
      list-style: none;
    }

    ul a {
      padding: 10px;
    }

    li img {
      width: 20px;
      height: 20px;

      &:hover {
        border: 1px dashed #00cffd;
        width: 30px;
        border-radius: 8px;
        transition: var(--transition);
      }
    }
  }

  .design-build-destination {
    h3 {
      color: var(--darkest-slate);
      font-size: 13px;
      font-weight: 300;
      line-height: 1;
      padding: 10px;
    }
    a {
      text-decoration: none;
      img {
        text-align: center;
        align-items: center;
        margin: 0px 5px;

        &:hover {
          border: 1px dashed var(--color-focus);
          padding: 5px;
          border-radius: 10px;
          transition: var(--transition);
          animation-delay: var(--easing);
        }
      }
    }
  }
}
</style>