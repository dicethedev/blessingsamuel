<template>
  <section class="work-me">
    <div class="button-style">
      <h2 class="head-numbering">
        <span>03.</span> I’ve Worked here
        <div class="button-style2"></div>
      </h2>
    </div>

    <!-- Card here -->
    <div class="work-experience">
      <div class="experience-list">
        <!-- 1 -->
        <div class="experience-card">
          <h2>Software Engineer Intern</h2>
          <h4>Printrite.ng</h4>
          <ul>
            <li>
              <p>Did my internship program at Printrite Ng.</p>
            </li>
            <li>
              <p>
                Work with languagues , platforms , frameworks, and content
                management systems such as PHP, VueJs, Github, Bitbucket,
                JavaScript, SQL and Figma.
              </p>
            </li>
            <li>
              <p>
                Communicate with integrative teams of developers, engineers,
                designers and clients.
              </p>
            </li>
          </ul>
        </div>
        <!-- 2 -->
        <div class="experience-card">
          <h2>Wordpress Web Developer</h2>
          <h4>Lettads.com.ng</h4>
          <ul>
            <li>
              <p>Did my internship program at Printrite Ng.</p>
            </li>
            <li>
              <p>
                Work with languagues , platforms , frameworks, and content
                management systems such as PHP, VueJs, Github, Bitbucket,
                JavaScript, SQL and Figma.
              </p>
            </li>
            <li>
              <p>
                Communicate with integrative teams of developers, engineers,
                designers and clients.
              </p>
            </li>
          </ul>
        </div>
        <!-- 3 -->
        <div class="experience-card">
          <h2>What Next?</h2>
          <h4>You decide!</h4>
          <p>
            Make a sweet offer and I might just be your next Frontend Enigneer.
            You know that's right!
          </p>
        </div>
      </div>
    </div>
    <router-view />
  </section>
</template>

<script>
export default {
  components: {},
  data() {
    return {};
  },
};
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

.work-me {
  position: relative;
  height: 100vh;
  visibility: visible;
  opacity: 1;
  transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
  transition: opacity 0.5s cubic-bezier(0.645, 0.045, 0.355, 1) 0.2s,
    transform 0.5s cubic-bezier(0.645, 0.045, 0.355, 1) 0.2s;
  margin-top: 1200px;
  margin-left: 380px;

  .button-style {
    color: var(--color-focus);
    background-color: transparent;
    border: 1px dashed var(--color-focus);
    border-radius: 0px 20px;
    padding: 1.25rem 1.88rem;
    word-spacing: 5px;
    width: 315px;
    height: 60px;
    //115px
    margin-top: 7.1875rem;
    line-height: 1;
    text-decoration: none;

    //Mobile - Tablet Responsiveness
    @include breakpoint-down(medium) {
      margin-left: 200px;
      width: 180px;
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
      width: 100%;
      font-size: clamp(26px, 5vw, var(--fz-heading));
      white-space: nowrap;
      transition: var(--transition);
    }

    h2 {
      font-size: 23px;
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
        width: 110px;
        height: 60px;
        cursor: pointer;
        margin-top: -47px;
        margin-left: 176px;

        //Mobile Responsiveness
        @include breakpoint-down(medium) {
          width: 34px;
          height: 25px;
          margin-top: -40px;
          margin-left: 136px;
        }
      }
    }
  }
  .work-experience {
    display: flex;
    align-items: center;
    //115px
    margin-top: 90px;

    //Tablet Responsiveness
    @include breakpoint-down(large) {
      margin-left: -200px;
    }

    //Mobile - Tablet Responsiveness
    @include breakpoint-down(medium) {
      margin-left: -200px;
    }

    //Mobile - Tablet Responsiveness
    @include breakpoint-up(medium) {
      margin-left: -200px;
    }

    @include breakpoint-up(xlarge) {
      margin-left: -10px;
    }

    //Mobile Responsiveness
    @include breakpoint-down(small) {
      margin-left: -280px;
    }

    .experience-list {
      display: flex;
      justify-content: space-between;
      // gap: 0.5rem;
      flex-wrap: wrap;
      width: 100%;
      padding-bottom: 20px;
      margin-right: 50px;

      //Tablet Responsiveness
      @include breakpoint-down(large) {
        justify-content: space-around;
        margin-right: 60px;
      }
    }

    .experience-card {
      width: 320px;
      max-width: 30%;
      min-width: 300px;
      min-height: 245px;
      background: #e6f1ff;
      //10px
      border-radius: 5px;
      padding: 30px 25px;
      margin-right: 15px;
      margin-bottom: 40px;
      color: #16294b;

      //Mobile Responsiveness
      @include breakpoint-down(small) {
        width: 350px;
        max-width: 30%;
        min-width: 300px;
        min-height: 200px;
        margin-left: -30px;
      }

      h2,
      h4 {
        margin-bottom: 20px;
      }
      h2 {
        color: #16294b;
        line-height: 1;
        font-size: 1.5rem;
      }
      h4 {
        color: #00cffd;
        font-size: 16px;
        font-style: italic;
        font-weight: 400;
      }

      ul {
        padding-left: 20px;

        li,
        p {
          font-size: 14px;
          line-height: 1.5;
        }
      }
    }

    .experience-card:last-of-type {
      background: var(--color-focus);
      margin-right: 0;

      //Mobile Responsiveness
      @include breakpoint-down(small) {
        margin-right: 15px;
      }

      //Tablet - Mobile Responsiveness
      @include breakpoint-down(medium) {
        margin-right: 15px;
      }
    }
    .experience-card:last-of-type h4,
    .experience-card:last-of-type p {
      color: #fff;
    }
    .experience-card:last-of-type p {
      font-size: 14px;
    }
  }
}
</style>