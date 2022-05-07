<template>
  <div
    class="
      button-style
      container
      animate__animated animate__bounce"
  >
    <h2 class="heading-numbering">
      <span>03.</span> I’ve Worked here
      <div class="button-style-2"></div>
    </h2>
  </div>
  <div class="experience-me" id="my-experience">
    <div class="experiences">
      <div class="experience-list">
        <!-- 1 -->
        <div class="experience-card">
          <h2>Software Engineer Intern</h2>
          <a href="https://printrite.ng/"><h4>Printrite.ng</h4></a>
          <ul>
            <li>
              <p>
                Communicate with integrative teams of developers, engineers,
                designers and clients resulting to good decision making.
              </p>
            </li>
            <li>
              <p>Wrote Javascript functions to make html table downloadable as pdf files.</p>
            </li>
             <li>
              <p>Contributing creative ideas during corporate brainstorming sessions at <a href="https://myshelta.com/">myshelta.com</a></p>
            </li>
          </ul>
        </div>
        <!-- 2 -->
        <div class="experience-card">
          <h2>WordPress Developer</h2>
          <a href="https://Lettads.com.ng/"><h4>Lettads.com.ng</h4></a>
          <ul>
             <li>
              <p>Frontend Developer</p>
            </li>
            <li>
              <p>
                Prioritizing workloads and coordinating multiple ongoing
                projects (Frontend prduct).
              </p>
            </li>
            <li>
              <p>
                Worked with the team to build a
                suitable functional e-commerce section on Lettads.
              </p>
            </li>
            <li>
              <p>
                Implementing Search Engine Optimization (SEO) and Search Engine
                Marketing (SEM) to get measurable results.
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

.button-style {
  background-color: transparent;
  border: 1px dashed var(--color-primary);
  border-radius: 0px 20px;
  padding: 1.25rem 1.88rem;
  word-spacing: 5px;
  width: 305px;
  height: 60px;
  text-decoration: none;

  @media (max-width: 767.98px) {
    width: 248px;
    height: 54px;
  }

  .head-numbering > h2 {
    position: relative;
    margin: 10px 0px 40px;
    margin-top: 40px;
    width: 100%;
    font-size: clamp(26px, 5vw, var(--fz-heading));
    white-space: nowrap;
  }

  h2 {
    font-size: 23px;
    font-weight: 500;
    color: #e6f1ff;

    //Mobile Responsiveness
    @include breakpoint-down(small) {
      font-size: 16px;
    }

    //Mobile Responsiveness
    @include breakpoint-down(medium) {
      font-size: 17px;
    }

    span {
      color: var(--color-primary);
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
  }

  .button-style-2 {
    background-color: var(--color-primary);
    border-radius: 0px 20px;
    padding: 1.25rem 1.88rem;
    width: 100px;
    height: 62px;
    cursor: pointer;
    margin-top: -48px;
    margin-left: 175px;

    @media (max-width: 424.98px) {
      width: 30px;
      height: 25px;
    }

     //Mobile Responsiveness
    @include breakpoint-down(medium) {
      margin-top: -41px;
      margin-left: 140px;
      width: 77px;
      height: 57px;
    }
  }
}

.experience-me {
  padding: 100px 10.944vw;

  .experiences {
    display: flex;
    align-items: center;

    .experience-list {
       display: flex;
       justify-content: space-between;
       flex-wrap: wrap;
       width: 100%;
       padding-bottom: 30px;
       margin-right: -50px;

       @media (max-width: 575.98px)
     {
      flex-direction: column;
      justify-content: flex-start;
      align-items: center;
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
      background: var(--light-slate);
      border-radius: 4px;
      padding: 30px 25px;
      margin-right: 15px;
      margin-bottom: 40px;
      color: var(--color-bg-variant);

      @media (max-width: 575.98px) {
        margin: 25px 0;
        padding: 30px 20px;
        max-width: 450px;
        width: 100%;
        min-width: unset;
        min-height: 200px;
      }

      h2,
      h4 {
        margin-bottom: 20px;
      }
      h2 {
        color: var(--color-bg-variant);
        line-height: 1;
        font-size: 1.5rem;

      @media (max-width: 374.98px) {
         font-size: 0.5;
        }
      }

      a {
        text-decoration: none;
      }

      h4 {
        color: var(--color-primary);
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
          a {
            color: var(--color-primary);
          }
        }
      }
    }

    .experience-card:last-of-type {
      background: var(--color-primary);
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