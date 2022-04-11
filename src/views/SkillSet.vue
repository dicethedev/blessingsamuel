<template>
  <div
    class="
      container
      button-style-1
      animate__animated animate__bounce animate__infinite
    "
  >
    <h2 class="heading-numbering">
      <span>04.</span> I’ve this Skillset
      <div class="button-style-2"></div>
    </h2>
  </div>
  <div class="skillset">
    <div class="skills">
      <div class="skill-container">
        <div class="skill-list">
          <img src="../assets/logos_html-5.svg" alt="" />
          <img src="../assets/logos_css-3.svg" alt="" />
          <img src="../assets/logos_sass.svg" alt="" />
          <img src="../assets/logos_javascript.svg" alt="" />
          <img src="../assets/logos_vue.svg" alt="" />
          <img src="../assets/logos_react.svg" alt="" />
          <img src="../assets/logos_mysql.svg" alt="" />
          <img src="../assets/logos_nodejs.svg" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
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
.button-style-1 {
  color: var(--color-focus);
  background-color: transparent;
  border: 1px dashed var(--color-focus);
  border-radius: 0px 20px;
  padding: 1.25rem 1.88rem;
  word-spacing: 5px;
  width: 305px;
  height: 60px;
  line-height: 1;
  text-decoration: none;
  cursor: pointer;
  margin-top: 90px;

  //Mobile Responsiveness
  @include breakpoint-down(medium) {
    width: 237px;
    height: 52px;
  }

  .heading-numbering > h2 {
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
    color: var(--light-slate);
    //Mobile Responsiveness
    @include breakpoint-down(medium) {
      font-size: 17px;
    }
    span {
      color: var(--color-focus);
      font-size: 19px;
      font-weight: 200;
      margin-right: 2px;
      //Mobile Responsiveness
      @include breakpoint-down(medium) {
        font-size: 16px;
      }
    }
    .button-style-2 {
      color: var(--color-focus);
      background-color: var(--color-focus);
      border-radius: 0px 20px;
      padding: 1.25rem 1.88rem;
      width: 127px;
      height: 61px;
      cursor: pointer;
      margin-top: -49px;
      margin-left: 147px;

      //Mobile Responsiveness
      @include breakpoint-down(medium) {
        margin-top: -41px;
        margin-left: 110px;
        width: 96px;
        height: 54px;
      }
    }
  }
}

.skillset {
  padding: 100px 6.944vw;
  // padding: 200px 15.944vw 150px;
  position: relative;

  @media (max-width: 991.98px) {
    padding: 150px 6.944vw;
  }

  .skills {
    display: flex;
    align-items: center;

    .skill-container {
      width: 80%;
      overflow: hidden;
      margin-top: 15px;

      .skill-list {
        display: flex;
        align-items: center;
        width: -webkit-fit-content;
        width: -moz-fit-content;
        width: fit-content;
        -webkit-animation: scrollFromLefttoRight 5s ease-in-out 1s infinite;
        animation: scrollFromLefttoRight 5s ease-in-out 1s infinite;

        @include breakpoint-down(medium) {
          -webkit-animation: scrollFromLefttoRight 4s ease-in-out 1s infinite;
          animation: scrollFromLefttoRight 4s ease-in-out 1s infinite;
        }

        img {
          margin-right: 15px;
          width: 120px;
          height: 120px;
        }

        @keyframes scrollFromLefttoRight {
          0% {
            -webkit-transform: translateX(0);
            transform: translateX(0);
          }
          50% {
            -webkit-transform: translateX(-55%);
            transform: translateX(-55%);
          }
          100% {
            -webkit-transform: translateX(0);
            transform: translateX(0);
          }
        }
      }
    }
  }
}
</style>