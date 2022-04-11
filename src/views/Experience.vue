<template>
  <div
    class="
      button-style-1
      container
      animate__animated animate__bounce animate__infinite
    "
  >
    <h2 class="heading-numbering">
      <span>02.</span> I’ve Worked here
      <div class="button-style-2"></div>
    </h2>
  </div>
  <div class="experience-me">
    <div class="experiences">
      <div class="experience-list">
        <!-- Card here -->
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
            <li>
              <p>I was able to build useful applications back to back.</p>
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
          <h2>What's Next?</h2>
          <h4>You decide!</h4>
          <p>
            Make a sweet offer and I might just be your next Frontend Software
            Enigneer. You know that's right!
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

.button-style-1 {
  // display: flex;
  // align-items: center;
  color: var(--color-focus);
  background-color: transparent;
  border: 1px dashed var(--color-focus);
  border-radius: 0px 20px;
  padding: 1.25rem 1.88rem;
  word-spacing: 5px;
  width: 305px;
  height: 55.5px;
  text-decoration: none;

  @media (max-width: 767.98px) {
    width: 260px;
    height: 54px;
  }

  .heading-numbering {
    font-size: 23px;
    font-weight: 500;
    color: #e6f1ff;

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
      @include breakpoint-down(medium) {
        font-size: 17px;
      }
    }
  }

  .button-style-2 {
    color: var(--color-focus);
    background-color: #00cffd;
    border-radius: 0px 20px;
    padding: 1.25rem 1.88rem;
    width: 100px;
    height: 60px;
    cursor: pointer;
    margin-top: -48px;
    margin-left: 175px;

    @media (max-width: 424.98px) {
      width: 30px;
      height: 25px;
    }

    //Mobile Responsiveness
    @include breakpoint-down(medium) {
      margin-top: -42px;
      margin-left: 150px;
      width: 80px;
      height: 55px;
    }
  }
}

.experience-me {
  padding: 100px 7.944vw;

  .experiences {
    display: flex;
    align-items: center;
    // margin-top: 30px;

    .experience-list {
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
      width: 100%;
      padding-bottom: 30px;
      margin-left: 100px;

      //Mobile Responsiveness
      @include breakpoint-down(small) {
        flex-direction: column;
        justify-content: flex-start;
        align-items: center;
        margin-left: 100px;
      }

      //Mobile Responsiveness
      @include breakpoint-down(medium) {
        margin-left: 10px;
      }

      @media (max-width: 1199.98px) {
        justify-content: space-around;
        margin-right: -90px;
      }
    }

    .experience-card {
      width: 350px;
      max-width: 30%;
      min-width: 300px;
      min-height: 245px;
      background: #e6f1ff;
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

      // @media (max-width: 575.98px) {
      //   margin: 25px 0;
      //   padding: 30px 20px;
      //   max-width: 450px;
      //   width: 100%;
      //   min-width: unset;
      //   min-height: 200px;
      // }

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