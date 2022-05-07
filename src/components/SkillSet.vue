<template>
  <div
    class="
      container
      button-style-1
      animate__animated animate__bounce"
  >
    <h2 class="heading-numbering">
      <span>04.</span> I’ve this Skillset
      <div class="button-style-2"></div>
    </h2>
  </div>
  <div class="skillset" id="skill-set">
    <div class="skills">
      <div class="skill-container">
        <div class="skill-list">
          <img src="../assets/logos_html-5.svg" alt="" />
          <img src="../assets/logos_css-3.svg" alt="" />
          <img src="../assets/logos_sass.svg" alt="" />
          <img src="../assets/logos_javascript.svg" alt="" />
          <img src="../assets/logos_vue.svg" alt="" />
          <img src="../assets/logos_react.svg" alt="" />
          <img src="../assets/logos_typescript.svg" alt="" />
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
   --color-bg: #1f1f38;
  --color-bg-variant: #2c2c6c;
  --color-loader: #22224e;
  --color-primary: #4db5ff;
  --color-primary-variant: rgba(77, 181, 255, 0.4);
  --color-focus: #00cffd;
  --fz-sm: 13px;
  --fz-md: 18px;
  --fz-heading: 32px;
  --normal-slate: #a8b2d1;
  --lightest-slate: #ccd6f6;
  --light-slate: #e6f1ff;
  --darkest-slate: #8892b0;
  
     ---container-width-lg: 75%;
     ---container-width-md: 86%;
     ---container-width-sm: 90%; 
  --transition: all 0.25s cubic-bezier(0.645, 0.045, 0.355, 1);
  --easing: cubic-bezier(0.645, 0.045, 0.355, 1);
  --animate-duration: 0.4ms;
  --animate-delay: 400ms;
}

html {
     scroll-behavior: smooth;
}

.button-style-1 {
  background-color: transparent;
  border: 1px dashed var(--color-primary);
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
          @include breakpoint-down(small) {
            font-size: 16px;
          }

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
      background-color: var(--color-primary);
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
    padding: 100px 20.944vw;
    position: relative;

  .skills {
    display: flex;
    align-items: center;

    .skill-container {
      width: 100%;
      overflow: hidden;
      margin-right: -90px;
      margin-top: 15px;

      @media (max-width: 991.98px) {
      margin-top: 0;
     }

      .skill-list {
        display: flex;
        align-items: center;
        width: -webkit-fit-content;
        width: -moz-fit-content;
        width: fit-content;
        -webkit-animation: scrollFromLefttoRight 5s ease-in-out 1s infinite;
        animation: scrollFromLefttoRight 5s ease-in-out 1s infinite;

        @media (max-width: 767.98px){
         -webkit-animation: scrollFromLefttoRight 2s ease-in-out 1s infinite;
         animation: scrollFromLefttoRight 2s ease-in-out 1s infinite;
        }

        @media (max-width: 1199.98px){
         -webkit-animation: scrollFromLefttoRight 8s ease-in-out 1s infinite;
         animation: scrollFromLefttoRight 8s ease-in-out 1s infinite;
        }

        img {
          width: 100px;
          height: 100px;
          margin-right: 20px;

          @media (max-width: 575.98px) {
           margin-right: -40px;
          }

          @media (max-width: 575.98px) {
            -webkit-transform: scale(0.6);
            transform: scale(0.6);
            margin-right: -20px;
          }

          @media (max-width: 991.98px) {
            -webkit-transform: scale(0.8);
            transform: scale(0.8);
            margin-right: -10px;
          }
        }

        @keyframes scrollFromLefttoRight {
          0% {
            -webkit-transform: translateX(0);
            transform: translateX(0);
          }
          50% {
            -webkit-transform: translateX(-68%);
            transform: translateX(-68%);
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