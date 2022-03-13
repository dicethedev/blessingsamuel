<template>
  <section class="work-me">
    <div class="button-style">
      <h2 class="head-numbering">
        <span>02.</span> I’ve Worked here
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
  margin-top: 90px;
  margin-left: 380px;

  .button-style {
    color: var(--color-focus);
    background-color: transparent;
    border: 1px dashed var(--color-focus);
    border-radius: 0px 30px;
    padding: 1.25rem 1.88rem;
    word-spacing: 5px;
    width: 260px;
    //115px
    margin-top: 7.1875rem;
    height: 30px;
    line-height: 1;
    text-decoration: none;
    cursor: pointer;
    transition: var(--transition);

    //Tablet Responsiveness
    @include breakpoint-down(medium) {
      margin-left: -350px;
      width: 180px;
      height: 20px;
    }

    //Mobile Responsiveness
    @include breakpoint-down(small) {
      margin-left: 800px;
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
      font-size: 25px;
      font-weight: 700;
      color: #ccd6f6;
      //Mobile Responsiveness
      @include breakpoint-down(medium) {
        font-size: 17px;
      }
      span {
        color: #00cffd;
        font-size: 20px;
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
        border-radius: 0px 30px;
        padding: 1.25rem 1.88rem;
        width: 42px;
        height: 35px;
        cursor: pointer;
        margin-top: -49px;
        margin-left: 190px;

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
    margin-top: 7.1875rem;
    // padding: 100px 6.944vw;

    .experience-list {
      display: grid;
      grid-template-columns: 1fr;
      gap: 0.5rem;
      width: 100%;
      padding-bottom: 30px;
      margin-right: 3.125rem;

      @include breakpoint-up(medium) {
        grid-template-columns: repeat(2, 1fr);
        margin-left: -300px;
      }
      //Responsiveness for Desktop or Laptop
      @include breakpoint-up(large) {
        grid-template-columns: repeat(3, 1fr);
        margin-left: -2px;
      }

      //Tablet Responsiveness
      @include breakpoint-down(medium) {
        grid-template-columns: repeat(1, 1fr);
        margin-left: -280px;
      }

      //Mobile Responsiveness
      @include breakpoint-down(small) {
        margin-left: -380px;
      }

      //Responsiveness for Desktop or Laptop
      @include breakpoint-down(large) {
        grid-template-columns: repeat(2, 1fr);
        margin-left: -100px;
        gap: 1px;
      }
    }

    .experience-card {
      width: 300px;
      max-width: 20%;
      min-width: 300px;
      min-height: 200px;
      background: #e6f1ff;
      //10px
      border-radius: 0.625rem;
      padding: 30px 25px;
      margin-right: 15px;
      margin-bottom: 40px;
      color: #16294b;

      //Mobile Responsiveness
      @include breakpoint-down(small) {
        width: 350px;
        max-width: 50%;
        min-width: 350px;
        min-height: 200px;
        margin-left: -30px;
      }
      //Tablet Responsiveness
      @include breakpoint-down(medium) {
        width: 350px;
        max-width: 50%;
        min-width: 350px;
        min-height: 200px;
        margin-left: 60px;
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

    .experience-card:nth-child(2) {
      //Responsiveness for Desktop or Laptop
      @include breakpoint-down(large) {
        margin-left: -150px;
      }
    }

    .experience-card:last-of-type {
      background: var(--color-focus);
      margin-right: 0;

      //Responsiveness for Desktop or Laptop
      @include breakpoint-down(large) {
        margin-left: 200px;
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