<template>
  <section class="project-me">
    <div class="button-style">
      <h2 class="head-numbering">
        <span>02.</span> I’ve Built this
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
        <div class="container">
          <p>
            Weather app develop with Vue. An API is pass from openweather.org,
            You can search any country of your choice from the web app and it
            will tell you the country tempeature, date, time, atmosphere
            changes. Having struggled understanding how to pass an API through
            this I learn a lot from my struggle.
          </p>
        </div>
        <div class="stacks">
          <div class="stack">HTMl</div>
          <div class="stack">CSS</div>
          <div class="stack">VUE</div>
          <div class="stack">API</div>
        </div>

        <div class="link-direction">
          <a
            href="https://toye-quiz.netlify.app/"
            target="_blank"
            rel="noreferrer"
          >
            <img src="../assets/github-link-direct.svg" alt="" />
          </a>
          <a
            href="https://toye-quiz.netlify.app/"
            target="_blank"
            rel="noreferrer"
          >
            <img class="lmg-2" src="../assets/arrow-link-direct.svg" alt="" />
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
        <div class="container">
          <p>
            Weather app develop with Vue. An API is pass from openweather.org,
            You can search any country of your choice from the web app and it
            will tell you the country tempeature, date, time, atmosphere
            changes. Having struggled understanding how to pass an API through
            this I learn a lot from my struggle.
          </p>
        </div>
        <div class="stacks">
          <div class="stack">HTMl</div>
          <div class="stack">CSS</div>
          <div class="stack">VUE</div>
          <div class="stack">API</div>
        </div>

        <div class="link-direction">
          <a
            href="https://toye-quiz.netlify.app/"
            target="_blank"
            rel="noopener noreferrer"
          >
            <img src="../assets/github-link-direct.svg" alt="" />
          </a>
          <a
            href="https://toye-quiz.netlify.app/"
            target="_blank"
            rel="noopener noreferrer"
          >
            <img src="../assets/arrow-link-direct.svg" alt="" />
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
        <div class="container">
          <p>
            Weather app develop with Vue. An API is pass from openweather.org,
            You can search any country of your choice from the web app and it
            will tell you the country tempeature, date, time, atmosphere
            changes. Having struggled understanding how to pass an API through
            this I learn a lot from my struggle.
          </p>
        </div>
        <div class="stacks">
          <div class="stack">HTMl</div>
          <div class="stack">CSS</div>
          <div class="stack">VUE</div>
          <div class="stack">API</div>
        </div>

        <div class="link-direction">
          <a
            href="https://toye-quiz.netlify.app/"
            target="_blank"
            rel="noreferrer"
          >
            <img src="../assets/github-link-direct.svg" alt="" />
          </a>
          <a
            href="https://toye-quiz.netlify.app/"
            target="_blank"
            rel="noreferrer"
          >
            <img class="lmg-2" src="../assets/arrow-link-direct.svg" alt="" />
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
  --fz-sm: 12px;
  --fz-md: 16px;
  --fz-heading: 32px;
  --lightest-slate: #ccd6f6;
  --easing: cubic-bezier(0.645, 0.045, 0.355, 1);
  --transition: all 0.25s cubic-bezier(0.645, 0.045, 0.355, 1);
  --dice-color-shadow: rgba(2, 12, 27, 0.7);
}

.project-me {
  position: relative;
  height: 100vh;
  visibility: visible;
  opacity: 1;
  transition: opacity 0.5s cubic-bezier(0.645, 0.045, 0.355, 1) 0.2s,
    transform 0.5s cubic-bezier(0.645, 0.045, 0.355, 1) 0.2s;
  margin-top: 90px;
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
    margin-top: 120px;

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
      margin-left: -255px;
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
      color: #ccd6f6;
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
        background-color: #00cffd;
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
    // margin-right: 300px;
    position: relative;
    margin-top: 90px;
    margin-bottom: 60px;

    .image-container {
      //Mobile responsiveness
      // padding: 40px;
      // width: 34.24vw;
      // height: 34.24vw;
      background: #d9e4f3;
      padding: 20px;
      border-radius: 3px;
      width: 27.24vw;
      height: 27.24vw;

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
      margin-left: -90px;

      h1 {
        color: #0db9ff;
        font-size: var(--fz-md);
        font-weight: 200;
        font-style: italic;
        line-height: 1.5;
        margin-bottom: 10px;
        margin-left: 400px;
      }
      h3 {
        color: #e6f1ff;
        font-size: 30px;
        font-weight: 400px;
        margin-left: 355px;
        margin-bottom: 20px;
      }
    }

    .container {
      display: flex;
      position: relative;
      background: #16294b;
      box-shadow: 4px 7px 57px 2px rgba(0, 0, 0, 0.25);
      border-radius: 5px;
      padding: 15px;

      p {
        font-size: 16px;
        line-height: 1.5;
        text-align: right;
        color: #8892b0;
        font-weight: 300;
      }
    }

    .stacks {
      display: flex;
      margin-top: 20px;
      margin-bottom: 16px;
      margin-left: 180px;

      .stack {
        display: flex;
        width: 80px;
        height: 32px;
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
      -webkit-box-align: center;
      align-items: center;
      position: relative;
      margin-top: 10px;
      margin-left: 420px;

      a {
        display: flex;
        -webkit-box-pack: center;
        justify-content: center;
        -webkit-box-align: center;
        align-items: center;
        padding: 10px;
        img {
          width: 25px;
          &:hover {
            border: 1px dashed #00cffd;
            padding: 10px;
            border-radius: 20px;
          }
        }
      }
    }
  }
}
</style>