<template>
  <section class="project-me">
    <div
      class="button-style animate__animated animate__bounce animate__infinite"
    >
      <h2 class="head-numbering">
        <span>03.</span> I’ve Built this
        <div class="button-style2"></div>
      </h2>
    </div>

    <!-- 1 -->
    <div class="project-content">
      <div class="image-container">
        <a href=""
          ><img src="../assets/project-image-1.jpg" alt="project-image-1"
        /></a>
      </div>
      <div class="project-details">
        <h1>Featured Project</h1>
        <h3>Weather App</h3>
        <p>
          Weather app develop with Vue. An API is pass from openweather.org, You
          can search any country of your choice from the web app and it will
          tell you the country tempeature, date, time, atmosphere changes.
          Having struggled understanding how to pass an API through this I learn
          a lot from my struggle.
        </p>
        <div class="stacks">
          <div class="stack">HTMl</div>
          <div class="stack">CSS</div>
          <div class="stack">VUE.JS</div>
          <div class="stack">API</div>
        </div>

        <div class="link-direction">
          <a
            href="https://github.com/dicethedev/Weatherapp"
            target="_blank"
            rel="noreferrer"
          >
            <img src="../assets/akar-icons_github-fill.svg" alt="github" />
          </a>
          <a
            href="https://weatherappbyblessing.vercel.app/"
            target="_blank"
            rel="noreferrer"
          >
            <img
              src="../assets/bi_arrow-right-circle-fill.svg"
              alt="arrow-right"
            />
          </a>
        </div>
      </div>
    </div>

    <!-- 2 -->
    <div class="project-content">
      <div class="image-container">
        <a href=""
          ><img src="../assets/project-image-2.jpg" alt="project-image-1"
        /></a>
      </div>
      <div class="project-details">
        <h1>Featured Project</h1>
        <h3>Weather App</h3>

        <p>
          Weather app develop with Vue. An API is pass from openweather.org, You
          can search any country of your choice from the web app and it will
          tell you the country tempeature, date, time, atmosphere changes.
          Having struggled understanding how to pass an API through this I learn
          a lot from my struggle.
        </p>

        <div class="stacks">
          <div class="stack">HTMl</div>
          <div class="stack">CSS</div>
          <div class="stack">VUE</div>
          <!-- <div class="stack">VUE</div> -->
          <div class="stack">FIREBASE</div>
        </div>

        <div class="link-direction">
          <a href="#" target="_blank" rel="noopener noreferrer">
            <img src="../assets/akar-icons_github-fill.svg" alt="github" />
          </a>
          <a href="#" target="_blank" rel="noopener noreferrer">
            <img
              src="../assets/bi_arrow-right-circle-fill.svg"
              alt="arrow-right"
            />
          </a>
        </div>
      </div>
    </div>

    <!-- 3 -->
    <div class="project-content">
      <div class="image-container">
        <a href=""
          ><img src="../assets/project-image-1.jpg" alt="project-image-1"
        /></a>
      </div>
      <div class="project-details">
        <h1>Featured Project</h1>
        <h3>Weather App</h3>

        <p>
          Weather app develop with Vue. An API is pass from openweather.org, You
          can search any country of your choice from the web app and it will
          tell you the country tempeature, date, time, atmosphere changes.
          Having struggled understanding how to pass an API through this I learn
          a lot from my struggle.
        </p>

        <div class="stacks">
          <div class="stack">HTMl</div>
          <div class="stack">CSS</div>
          <div class="stack">VUE.JS</div>
          <div class="stack">API</div>
        </div>

        <div class="link-direction">
          <a href="#" target="_blank" rel="noreferrer">
            <img src="../assets/akar-icons_github-fill.svg" alt="github" />
          </a>
          <a href="#" target="_blank" rel="noreferrer">
            <img src="../assets/bi_arrow-right-circle-fill.svg" alt="Vector" />
          </a>
        </div>
      </div>
    </div>
  </section>
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

.project-me {
  position: relative;
  height: 100vh;
  margin-top: 100px;
  margin-left: 380px;

  .button-style {
    color: var(--color-focus);
    background-color: transparent;
    border: 1px dashed var(--color-focus);
    border-radius: 0px 20px;
    padding: 1.25rem 1.88rem;
    word-spacing: 5px;
    width: 290px;
    height: 60px;
    line-height: 1;
    text-decoration: none;
    cursor: pointer;
    margin-left: 240px;

    //Mobile Responsiveness
    @include breakpoint-down(small) {
      margin-left: 200px;
      margin-top: 500px;
      width: 170px;
      height: 20px;
    }

    //Mobile Responsiveness
    @include breakpoint-down(medium) {
      margin-left: -310px;
      margin-top: 500px;
      width: 170px;
      height: 20px;
    }

    //Responsiveness for Desktop or Laptop
    @include breakpoint-down(large) {
      margin-left: 150px;
    }

    //Responsiveness for Desktop or Laptop
    @include breakpoint-up(xlarge) {
      margin-left: 340px;
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
      color: var(--light-slate);
      //Mobile Responsiveness
      @include breakpoint-down(medium) {
        font-size: 17px;
      }
      span {
        color: #00cffd;
        font-size: 19px;
        font-weight: 200;
        margin-right: 2px;
        //Mobile Responsiveness
        @include breakpoint-down(medium) {
          font-size: 16px;
        }
      }
      .button-style2 {
        color: var(--color-focus);
        background-color: var(--color-focus);
        border-radius: 0px 20px;
        padding: 1.25rem 1.88rem;
        width: 101px;
        height: 60px;
        cursor: pointer;
        margin-top: -49px;
        margin-left: 157px;

        //Mobile Responsiveness
        @include breakpoint-down(medium) {
          width: 34px;
          height: 25px;
          margin-top: -41px;
          margin-left: 115px;
        }
      }
    }
  }

  .project-content {
    display: flex;
    align-items: center;
    margin-bottom: 200px;
    width: 100%;
    justify-content: space-between;
    position: relative;
    margin-top: 100px;
    margin-bottom: 60px;
    flex-direction: row;

    &:nth-last-of-type(2n) {
      flex-direction: row-reverse;
      // margin-left: -70px;
    }

    //Responsiveness for Desktop or Laptop
    @include breakpoint-down(large) {
      margin-left: -50px;
    }

    .image-container {
      background: var(--light-slate);
      padding: 25px;
      border-radius: 5px;
      width: 28.24vw;
      height: 28.24vw;

      //Responsiveness for Desktop or Laptop
      @include breakpoint-down(large) {
        padding: 15px;
      }

      img {
        object-fit: cover;
        object-position: left center;
        width: 100%;
        height: 100%;
        border-radius: 3px;
      }
    }

    .project-details {
      width: 36vw;
      margin-left: 60px;

      //Responsiveness for Desktop or Laptop
      @include breakpoint-down(large) {
        width: 40vw;
      }

      h1 {
        color: #0db9ff;
        font-size: var(--fz-md);
        font-weight: 200;
        font-style: italic;
        line-height: 1.5;
        margin-bottom: 10px;
        // margin-left: 250px;
      }

      h3 {
        color: var(--light-slate);
        font-size: clamp(24px, 5vw, 28px);
        font-weight: 400px;
        // margin-left: 215px;
        margin-bottom: 20px;

        //Responsiveness for Desktop or Laptop
        @include breakpoint-down(large) {
          font-size: clamp(25px, 5vw, 18px);
          margin-right: -500px;
        }
      }

      p {
        font-size: 16px;
        line-height: 1.5;
        color: var(--darkest-slate);
        font-weight: 300;
        max-width: 300px;
      }

      .stacks {
        display: flex;
        margin-top: 30px;
        margin-bottom: 16px;

        //Responsiveness for Desktop or Laptop
        @include breakpoint-down(large) {
          // margin-right: 300px;
        }

        .stack {
          display: flex;
          width: 80px;
          height: 30px;
          justify-content: center;
          align-items: center;
          background: var(--color-focus);
          color: #112240;
          border-radius: 5px;
          margin-right: 10px;
          letter-spacing: 0.2em;
          font-size: 12px;
        }
      }

      .link-direction {
        display: flex;
        margin-top: 10px;

        a {
          display: inline-block;
          -webkit-box-pack: center;
          justify-content: center;
          -webkit-box-align: center;
          align-items: center;
          padding: 8px;

          img {
            width: 20px;

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
  }
}
</style>