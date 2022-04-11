<template>
  <div class="contact-me">
    <div
      class="button-style-1 animate__animated animate__bounce animate__infinite"
    >
      <h2 class="head-numbering">
        <span>05.</span> What’s Next?
        <div class="button-style-2"></div>
      </h2>
    </div>

    <div class="contact-details">
      <h1>Get me Hired!</h1>
      <p>
        I'm looking for any new opportunities, my inbox is always open. If
        you’re currently have a role for Blessing, please don’t hestiate to get
        in touch with me. I’ll try all my best to reply you on time. Thank you!
      </p>
      <button class="contact-link">
        <a :href="`mailto:${email}`">Say Hello</a>
      </button>
    </div>
  </div>

  <footer>
    <h3>Designed & Built by Blessing Samuel</h3>
    <div class="project-destination">
      <a
        href="https://www.figma.com/file/FrJ9xgmbpnefZUTFBr0CNE/Blessing-Samuel-Portfolio?node-id=0%3A1"
        target="_blank"
        rel="noreferrer"
        ><img src="../assets/fa-brands_figma.svg" alt="figma"
      /></a>
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
  --color-focus: #00cffd;
  --fz-sm: 12px;
  --fz-md: 16px;
  --fz-heading: 32px;
  --lightest-slate: #ccd6f6;
  --easing: cubic-bezier(0.22, 0.68, 0, 1.71);
  --transition: all 0.25s cubic-bezier(0.645, 0.045, 0.355, 1);
  --dice-color-shadow: rgba(2, 12, 27, 0.7);
}

.contact-me {
  .button-style-1 {
    color: var(--color-focus);
    background-color: transparent;
    border: 1px dashed var(--color-focus);
    border-radius: 0px 20px;
    padding: 1.25rem 1.88rem;
    word-spacing: 5px;
    width: 275px;
    height: 60px;
    line-height: 1;
    text-decoration: none;
    margin-top: 100px;
    margin-left: 620px;

    //Mobile Responsiveness
    @include breakpoint-down(small) {
      margin-left: 200px;
      margin-top: 500px;
      width: 170px;
      height: 20px;
    }

    //Mobile Responsiveness
    @include breakpoint-down(medium) {
      margin-left: 230px;
      margin-top: 120px;
      width: 220px;
      height: 50px;
    }

    .head-numbering > h2 {
      display: flex;
      -webkit-box-align: center;
      justify-content: center;
      align-items: center;
      position: relative;
      margin: 10px 0px 40px;
      width: 100%;
      font-size: clamp(26px, 5vw, var(--fz-heading));
      white-space: nowrap;
    }

    h2 {
      font-size: 25px;
      font-weight: 700;
      color: #e6f1ff;

      //Mobile Responsiveness
      @include breakpoint-down(small) {
        font-size: 17px;
      }
      //Mobile Responsiveness
      @include breakpoint-down(medium) {
        font-size: 18px;
      }
      span {
        color: #00cffd;
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
        color: var(--color-focus);
        background-color: #00cffd;
        border-radius: 0px 20px;
        padding: 1.25rem 1.88rem;
        width: 120px;
        height: 60px;
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

  .contact-details {
    margin-top: 70px;
    margin-left: 450px;
    max-width: 600px;
    text-align: center;

    //Mobile Responsiveness
    @include breakpoint-down(medium) {
      margin-top: 50px;
      margin-left: 35px;
    }

    h1 {
      font-size: clamp(40px, 5vw, 55px);
      font-style: italic;
      color: var(--lightest-slate);
    }

    p {
      color: #8892b0;
      font-size: var(--fz-md);
      font-weight: 200;
      line-height: 26.44px;
      margin-top: 20px;

      //Mobile Responsiveness
      @include breakpoint-down(small) {
        margin-left: 200px;
      }
    }

    .contact-link {
      text-align: center;
      font-size: 16px;
      font-weight: 300;
      word-spacing: 5px;
      color: var(--green);
      background-color: transparent;
      border: 1px solid var(--color-focus);
      border-radius: 10px;
      padding: 1.25rem 1.75rem;
      width: fit-content;
      margin-top: 30px;
      overflow: hidden;

      a {
        text-decoration: none;
        color: var(--color-focus);
        cursor: pointer;
      }
    }
  }
}

footer {
  display: flex;
  -webkit-box-pack: center;
  justify-content: center;
  -webkit-box-align: center;
  align-items: center;
  flex-direction: column;
  height: auto;
  min-height: 70px;
  padding: 15px;
  text-align: center;
  margin-top: 200px;
  margin-left: 50px;

  //Mobile Responsiveness
  @include breakpoint-down(medium) {
    margin-top: 150px;
    margin-left: 10px;
  }

  h3 {
    color: #8892b0;
    font-size: 14px;
    font-weight: 300;
  }

  .project-destination {
    margin-top: 10px;
    a {
      text-decoration: none;

      img {
        margin-right: 5px;

        &:hover {
          border: 1px dashed #00cffd;
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