<template>
  <section class="about-me">
    <div
      class="button-style animate__animated animate__bounce animate__infinite"
    >
      <h2 class="head-numbering">
        <span>01.</span>About Me
        <div class="button-style2"></div>
      </h2>
    </div>

    <div class="container">
      <div class="container-details">
        <div class="details-1">
          <img src="@/assets/Profile.jpg" alt="" />
        </div>

        <div class="details-2">
          <p>
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
          <p>
            I was born in Kogi State, Nigeria. I graduated with a second class
            upper division in Sofwtare Engineering in Nigeria. I look forward to
            expanding my talent in the backend development.
          </p>
          <!-- <p>Here are a few technologies l’ve been working with recently:</p> -->
        </div>
      </div>
    </div>

    <div class="focus-line-heading"></div>
    <router-view />
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "/src/scss/_mixins.scss";
:root {
  --color-focus: #00cffd;
  --fz-sm: 12px;
  --fz-md: 16px;
  --fz-heading: 32px;
  --lightest-slate: #ccd6f6;
  --easing: cubic-bezier(0.645, 0.045, 0.355, 1);
  --transition: all 0.25s cubic-bezier(0.645, 0.045, 0.355, 1);
  --dice-color-shadow: rgba(2, 12, 27, 0.7);
}
.about-me {
  position: relative;
  height: 100vh;
  visibility: visible;
  opacity: 1;
  transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
  transition: opacity 0.5s cubic-bezier(0.645, 0.045, 0.355, 1) 0.2s,
    transform 0.5s cubic-bezier(0.645, 0.045, 0.355, 1) 0.2s;
  margin-top: 90px;
  margin-left: 420px;

  .button-style {
    color: var(--color-focus);
    background-color: transparent;
    border: 1px dashed #00e9df;
    border-radius: 0px 20px;
    padding: 1.25rem 1.88rem;
    word-spacing: 5px;
    width: 220px;
    height: 60px;
    line-height: 1;
    text-decoration: none;
    margin-left: 240px;

    //Tablet Responsiveness
    @include breakpoint-down(medium) {
      width: 140px;
      height: 20px;
    }

    //Responsiveness for Desktop or Laptop
    @include breakpoint-down(large) {
      margin-left: -180px;
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
      @include breakpoint-down(medium) {
        font-size: 17px;
      }
      span {
        color: #00cffd;
        font-size: 19px;
        font-weight: 200;
        margin-right: 10px;
        //Mobile Responsiveness
        @include breakpoint-down(medium) {
          font-size: 16px;
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
        @include breakpoint-down(medium) {
          width: 34px;
          height: 25px;
          margin-top: -40px;
          margin-left: 85px;
        }
      }
    }
  }

  .container {
    display: flex;
    width: 95vw;
    max-width: 500px;
    padding: 2rem;
    background-color: rgba(17, 34, 64, 1);
    padding: 1.5rem;
    margin-top: 4.375rem;
    border-radius: 30px;
    background-color: transparent;
    border: 1px solid;
    border-color: #00cffd #00e9df #00cffd #00e9df;
    // overflow: hidden;

    //Tablet Responsiveness
    @include breakpoint-down(large) {
      margin-left: -20px;
    }

    //Mobile - Tablet Responsiveness
    @include breakpoint-down(medium) {
      margin-left: -200px;
      max-width: 380px;
    }

    //Tablet Responsiveness
    @include breakpoint-down(small) {
      margin-left: -320px;
      max-width: 370px;
      overflow-x: hidden;
    }

    //Desktop Responsiveness
    @include breakpoint-up(xlarge) {
      margin-left: 200px;
    }

    .container-details {
      justify-content: center;
      align-items: center;
      text-align: center;

      .details-1 {
        img {
          display: flex;
          margin-top: 1.25rem;
          width: 8rem;
          margin-left: 10rem;
          clip-path: circle(60px at center);
          margin-bottom: 30px;

          // //Mobile Responsiveness
          // @include breakpoint-down(small) {
          //   margin-left: 4rem;
          //   margin-right: 2rem;
          // }

          //Mobile - Tablet Responsiveness
          @include breakpoint-down(medium) {
            margin-left: 8rem;
          }

          //Desktop Responsiveness
          @include breakpoint-up(large) {
            margin-left: 165px;
          }
        }
      }

      .details-2 {
        color: #8892b0;
        font-weight: 300;
        justify-content: center;
        align-items: center;
        margin-bottom: 1.25rem;

        p {
          margin-top: 10px;
          font-size: var(--fz-md);
          max-width: 500px;
          line-height: 25px;

          //Mobile Responsiveness
          @include breakpoint-down(small) {
            max-width: 500px;
          }
        }
      }
    }
  }
}

// @import "../assets/styles/_mixings-method.scss";
</style>

