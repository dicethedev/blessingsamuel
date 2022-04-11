<template>
  <div class="about-me">
    <div class="about-me-content">
      <div class="left">
        <div
          class="
            container
            button-style-1
            animate__animated animate__bounce animate__infinite
          "
        >
          <h2 class="head-numbering">
            <span>01.</span>About Me
            <div class="button-style-2"></div>
          </h2>
        </div>

        <div class="right">
          <img class="about-me-img" src="@/assets/Profile.jpg" alt="" />
        </div>
        <p class="about-paragraph">
          I am a Frontend Software Engineer currently based in Nigeria. I am
          very proficient using javascript and its frameworks like Vue & React.
          I am also very good with mock up languages such as html and css. I
          find joy when I use logic to provide solution to challenges thereby
          solving user potential problems. With three years of experience in
          frontend developement, I have been opportuned to build web apps that
          spread across different sectors such as education, estate management
          and finance.
        </p>
        <p class="about-paragraph">
          I was born in Kogi State, Nigeria. I graduated with a first class
          upper division in Software Engineering in Nigeria. My love for
          arithmetic and logic brought me towards the path of software
          development. I look forward to expanding my dexterity in the backend
          development.
        </p>
        <!-- <p>Here are a few technologies l’ve been working with recently:</p> -->
      </div>
    </div>
  </div>

  <!-- <div class="focus-line-heading"></div> -->
  <router-view />
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
  width: 100%;
  display: flex;
  align-items: center;
  padding: 200px 15.944vw 150px;
  overflow-y: hidden;
  position: relative;
  margin-top: -50px;

  .about-me-content {
    width: 100%;
    margin-right: -50px;

    .left {
      .button-style-1 {
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
        margin-bottom: 70px;

        //Mobile Responsiveness
        @include breakpoint-down(medium) {
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
          .button-style-2 {
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
    }

    .right {
      float: right;
      width: 44.7%;
      margin-left: 5.5%;
      margin-bottom: 30px;

      @media (max-width: 424.98px) {
        float: none;
        width: 100%;
        height: 400px;
        margin: 30px 0;
      }

      img {
        position: relative;
        border-radius: 3px;
        object-position: top center;
        max-height: 540px;
      }

      .about-me-img {
        width: 100%;
        height: 100%;
        object-fit: cover;
      }
    }
    .about-paragraph {
      font-size: 18px;
      line-height: 2;
      color: var(--lightest-slate);
      // font-weight: 200;
      margin-bottom: 46px;

      @media (max-width: 767.98px) {
        font-size: 16px;
        line-height: 1.7;
        margin-bottom: 32px;
      }

      @media (max-width: 424.98px) {
        font-size: 14px;
      }
    }
  }
}

// @import "../assets/styles/_mixings-method.scss";
</style>

