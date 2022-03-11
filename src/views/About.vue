<template>
  <section class="about-me">
    <div class="button-style">
      <h2 class="head-numbering">
        <span>01.</span>About Me
        <div class="button-style2"></div>
      </h2>
    </div>

    <div class="card">
      <div class="card-details">
        <div class="details-1">
          <img src="@/assets/Profile.jpg" alt="" />
        </div>

        <div class="details-2">
          <p>
            Hey, I’m Blessing Samuel by name and I love programming and
            designing things that live on the internet. My interest is web
            development and my web development journey started back then in 2019
            when I decided to try to work on a free HTML template. I am very
            adept using JavaScript and its frameworks like Vue & Angular. I can
            work with zeal and real wizardy.
          </p>
          <p>
            Blessing has a Diploma in Software Engineering. Blessing does not
            love talking about himself in the 3rd person. He want to learn New
            things, because that's what brings joy to his life Up. He believe in
            team success & growth, however he always put his best & maintain a
            strong team bonding for every project he get to work on. Here are a
            few technologies l’ve been working with recently: JavaScipt, Vue,
            Nodejs, GraphQl, TypeScript, MySQl & PHP.
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
  margin-left: 380px;

  //Mobile Responsiveness
  @include breakpoint-down(medium) {
    margin-left: 2.5rem;
  }

  .button-style {
    color: var(--color-focus);
    background-color: transparent;
    border: 1px dashed #00e9df;
    border-radius: 10px 30px;
    padding: 1.25rem 1.88rem;
    word-spacing: 5px;
    width: 160px;
    height: 30px;
    line-height: 1;
    text-decoration: none;
    cursor: pointer;
    transition: var(--transition);

    //Mobile Responsiveness
    @include breakpoint-down(medium) {
      margin-left: 2.5rem;
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
      transition: var(--transition);
    }

    h2 {
      font-size: 25px;
      font-weight: 700;
      color: #ccd6f6;
      span {
        color: #00cffd;
        font-size: 20px;
        font-weight: 200;
        margin-right: 10px;
      }
      .button-style2 {
        color: var(--color-focus);
        background-color: #00cffd;
        border-radius: 0px 30px;
        padding: 1.25rem 1.88rem;
        width: 16px;
        height: 35px;
        cursor: pointer;
        margin-top: -49px;
        margin-left: 115px;
      }
    }
  }

  .card {
    display: flex;
    position: relative;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    //800px
    width: 43.75rem;
    //600px
    height: 37.5rem;
    background-color: rgba(17, 34, 64, 1);
    padding: 1.5rem;
    top: 4.375rem;
    margin-left: -0.5rem;
    border-radius: 30px;
    background-color: transparent;
    border: 4px solid #00e9df;
    border-color: #00cffd #00e9df #00cffd #00e9df;

    //Mobile Responsiveness
    @include breakpoint-down(medium) {
      //400px
      width: 25rem;
      //570px
      height: 35.625rem;
    }

    .card-details {
      display: absolute;
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
          box-shadow: 0px 9px 57px -11px #00cffd;
          margin-bottom: 40px;

          //Mobile Responsiveness
          @include breakpoint-down(medium) {
            display: flex;
            margin-left: 8rem;
          }
        }
      }

      .details-2 {
        display: relative;
        color: #8892b0;
        font-weight: 400;
        justify-content: center;
        align-items: center;
        margin-bottom: 1.25rem;

        p {
          margin-top: 10px;
          font-size: 1.125rem;
          max-width: 500px;
          line-height: 25px;

          //Mobile Responsiveness
          @include breakpoint-down(medium) {
            font-size: 0.9375rem;
            line-height: 23px;
          }
        }
      }
    }
  }
}

// @import "../assets/styles/_mixings-method.scss";
</style>

