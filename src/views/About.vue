<template>
  <div class="about-me">
    <div
      class="button-style animate__animated animate__bounce animate__infinite"
    >
      <h2 class="head-numbering">
        <span>01.</span>About Me
        <div class="button-style2"></div>
      </h2>
    </div>

    <div class="about-content">
      <div class="about-me-content">
        <div class="left">
          <div class="right">
            <img class="about-me-img" src="@/assets/Profile.jpg" alt="" />
          </div>
          <p class="about-paragraph">
            I am a frontend software engineer currently based in Nigeria. I am
            very proficient using javascript and its frameworks like Vue and
            React. I am also very good with mock up languages such as html and
            css. I find joy when I use logic to provide solution to challenges
            thereby solving user potential problems. With two years of
            experience in frontend developement, I do not love talking about
            myself in the 3rd person. I want to learn New things, because that's
            what brings joy to my life Up. I believe in team success & growth,
            however I always put my best & maintain a strong team bonding for
            every project I get to work on.
          </p>
          <p class="about-paragraph">
            I was born in Kogi State, Nigeria. I graduated with a second class
            upper division in Sofwtare Engineering in Nigeria. I look forward to
            expanding my talent in the backend development.
          </p>
          <!-- <p>Here are a few technologies l’ve been working with recently:</p> -->
        </div>
      </div>
    </div>

    <!-- <div class="focus-line-heading"></div> -->
    <router-view />
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "/src/scss/_mixins.scss";
:root {
  --color-focus: #00cffd;
  --color-focus-fam: #00e9df;
  --fz-sm: 12px;
  --fz-md: 16px;
  --fz-heading: 32px;
  --lightest-slate: #ccd6f6;
  --light-slate: #e6f1ff;
  --darkest-slate: #8892b0;
  --easing: cubic-bezier(0.22, 0.68, 0, 1.71);
  --transition: all 0.25s cubic-bezier(0.645, 0.045, 0.355, 1);
  --animate-duration: 0.1ms;
  --animate-delay: 400ms;
  --dice-color-shadow: rgba(2, 12, 27, 0.7);
}

.about-me {
  position: relative;
  height: 100vh;
  margin-top: 90px;
  margin-left: 260px;

  .button-style {
    color: var(--color-focus);
    background-color: transparent;
    border: 1px dashed var(--color-focus-fam);
    border-radius: 0px 20px;
    padding: 1.25rem 1.88rem;
    word-spacing: 5px;
    width: 220px;
    height: 60px;
    line-height: 1;
    text-decoration: none;
    margin-left: 240px;

    //Mobile Responsiveness
    @include breakpoint-down(small) {
      margin-left: -280px;
      width: 190px;
      height: 52px;
    }

    //Mobile Responsiveness
    @include breakpoint-down(medium) {
      margin-left: -25px;
      width: 190px;
      height: 52px;
    }

    .head-numbering > h2 {
      display: flex;
      -webkit-box-align: center;
      justify-content: center;
      align-items: center;
      position: relative;
      margin: 10px 0px 40px;
      margin-top: 40px;
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
        font-size: 18px;
      }

      //Mobile Responsiveness
      @include breakpoint-down(medium) {
        font-size: 19px;
      }

      span {
        color: #00cffd;
        font-size: 19px;
        font-weight: 200;
        margin-right: 10px;

        //Mobile Responsiveness
        @include breakpoint-down(small) {
          font-size: 17px;
        }

        //Mobile Responsiveness
        @include breakpoint-down(medium) {
          font-size: 18px;
        }
      }
      .button-style2 {
        color: var(--color-focus);
        background-color: #00cffd;
        border-radius: 0px 20px;
        padding: 1.25rem 1.88rem;
        width: 75px;
        height: 60px;
        cursor: pointer;
        margin-top: -48px;
        margin-left: 115px;

        //Mobile Responsiveness
        @include breakpoint-down(small) {
          margin-top: -42px;
          margin-left: 95px;
          width: 63px;
          height: 53px;
        }

        //Mobile Responsiveness
        @include breakpoint-down(medium) {
          margin-top: -42px;
          margin-left: 95px;
          width: 64px;
          height: 53px;
        }
      }
    }
  }

  .about-content {
    margin-top: -90px;
    width: 100%;
    display: flex;
    align-items: center;
    padding: 200px 6.944vw 150px;
    overflow-y: hidden;

    //Mobile Responsiveness
    @include breakpoint-down(small) {
      margin-left: -390px;
      margin-top: -100px;
    }

    //Mobile Responsiveness
    @include breakpoint-down(medium) {
      margin-left: -125px;
    }

    .about-me-content {
      width: 100%;
      margin-right: -50px;

      .right {
        float: right;
        width: 44.7%;
        margin-left: 7.5%;
        margin-bottom: 30px;

        img {
          position: relative;
          border-radius: 3px;
          box-shadow: 0px 10px 30px rgba(0, 0, 0, 0.1);
          object-position: top center;
          max-height: 530px;
        }

        .about-me-img {
          width: 100%;
          height: 100%;
          object-fit: cover;
        }
      }
      .about-paragraph {
        font-size: 17px;
        line-height: 2;
        color: var(--lightest-slate);
        font-weight: 300;
        margin-bottom: 46px;

        //Mobile Responsiveness
        @include breakpoint-down(medium) {
          font-size: 16px;
          line-height: 1.7;
          margin-bottom: 32px;
        }
      }
    }
  }
}

// @import "../assets/styles/_mixings-method.scss";
</style>

