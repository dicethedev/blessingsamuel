<template>
  <div class="work-experience">
    <div
      class="button-style animate__animated animate__bounce animate__infinite"
    >
      <h2 class="head-numbering">
        <span>02.</span> I’ve Worked here
        <div class="button-style2"></div>
      </h2>
    </div>

    <!-- Card here -->
    <div class="experiences">
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
  </div>
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
  --easing: cubic-bezier(0.22, 0.68, 0, 1.71);
  --transition: all 0.25s cubic-bezier(0.645, 0.045, 0.355, 1);
  --dice-color-shadow: rgba(2, 12, 27, 0.7);
}

.work-experience {
  margin-top: 100px;
  margin-left: 380px;

  //Mobile Responsiveness
  @include breakpoint-down(small) {
    margin-top: 400px;
  }

  //Mobile Responsiveness
  @include breakpoint-down(medium) {
    margin-top: 300px;
  }

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
    margin-left: 240px;

    //Mobile Responsiveness
    @include breakpoint-down(small) {
      margin-left: -280px;
      width: 260px;
      height: 54px;
    }

    //Mobile Responsiveness
    @include breakpoint-down(medium) {
      margin-left: -180px;
      width: 260px;
      height: 54px;
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
        margin-right: 2px;

        //Mobile Responsiveness
        @include breakpoint-down(small) {
          font-size: 16px;
        }
        //Mobile Responsiveness
        @include breakpoint-down(medium) {
          font-size: 17px;
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
        @include breakpoint-down(small) {
          width: 79px;
          height: 55px;
          margin-top: -42px;
          margin-left: 150px;
        }
        //Mobile Responsiveness
        @include breakpoint-down(medium) {
          width: 79px;
          height: 55px;
          margin-top: -42px;
          margin-left: 150px;
        }
      }
    }
  }

  .experiences {
    display: flex;
    align-items: center;
    margin-top: 90px;

    //Mobile Responsiveness
    @include breakpoint-down(small) {
      margin-left: -300px;
    }

    @include breakpoint-down(medium) {
      margin-left: -200px;
    }

    .experience-list {
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
      width: 100%;
      padding-bottom: 20px;
      display: flex;
      margin-right: 50px;

      //Mobile Responsiveness
      @include breakpoint-down(small) {
        flex-direction: column;
        justify-content: flex-start;
        align-items: center;
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

      @include breakpoint-down(small) {
        margin: 25px 0;
        padding: 30px 20px;
        max-width: 400px;
        width: 100%;
        min-width: unset;
        min-height: 200px;
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