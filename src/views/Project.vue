<template>
  <div
    class="
      button-style-1
      container
      animate__animated animate__bounce animate__infinite
    "
  >
    <h2 class="heading-numbering">
      <span>03.</span> I’ve Built this
      <div class="button-style-2"></div>
    </h2>
  </div>

  <div class="my-project">
    <!-- 1 -->
    <div class="project">
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
            Weather app develop with Vue. An API is pass from openweather.org,
            You can search any country of your choice from the web app and it
            will tell you the country tempeature, date, time, atmosphere
            changes. Having struggled understanding how to pass an API through
            this I learn a lot from my struggle.
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
    </div>

    <!-- 2 -->
    <div class="project">
      <div class="project-content">
        <div class="image-container">
          <a href=""
            ><img src="../assets/project-image-2.jpg" alt="project-image-1"
          /></a>
        </div>
        <div class="project-details">
          <h1>Featured Project</h1>
          <h3>Invoice App</h3>

          <p>
            Weather app develop with Vue. An API is pass from openweather.org,
            You can search any country of your choice from the web app and it
            will tell you the country tempeature, date, time, atmosphere
            changes. Having struggled understanding how to pass an API through
            this I learn a lot from my struggle.
          </p>

          <div class="stacks">
            <div class="stack">HTMl</div>
            <div class="stack">VUE.JS</div>
            <div class="stack">VUEX</div>
            <!-- <div class="stack">VUE</div> -->
            <div class="stack">FIREBASE</div>
          </div>

          <div class="link-direction">
            <a href="#" target="_blank" rel="noopener noreferrer">
              <img src="../assets/akar-icons_github-fill.svg" alt="github" />
            </a>
            <a
              href="https://github.com/dicethedev/invoice-app"
              target="_blank"
              rel="noopener noreferrer"
            >
              <img
                src="../assets/bi_arrow-right-circle-fill.svg"
                alt="arrow-right"
              />
            </a>
          </div>
        </div>
      </div>
    </div>

    <!-- 3 -->
    <div class="project">
      <div class="project-content">
        <div class="image-container">
          <a href=""
            ><img src="../assets/project-image-1.jpg" alt="project-image-1"
          /></a>
        </div>
        <div class="project-details">
          <h1>Featured Project</h1>
          <h3>Screenshot App</h3>

          <p>
            Weather app develop with Vue. An API is pass from openweather.org,
            You can search any country of your choice from the web app and it
            will tell you the country tempeature, date, time, atmosphere
            changes. Having struggled understanding how to pass an API through
            this I learn a lot from my struggle.
          </p>

          <div class="stacks">
            <div class="stack">HTMl</div>
            <div class="stack">CSS</div>
            <div class="stack">VUE.JS</div>
            <div class="stack">NODE.JS</div>
          </div>

          <div class="link-direction">
            <a href="#" target="_blank" rel="noreferrer">
              <img src="../assets/akar-icons_github-fill.svg" alt="github" />
            </a>
            <a href="#" target="_blank" rel="noreferrer">
              <img
                src="../assets/bi_arrow-right-circle-fill.svg"
                alt="Vector"
              />
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  projectData: [
    {
      uniquename: "Featured Project",
      projectname: "Weather App",
      projectdescription:
        "  Weather app develop with Vue. An API is pass from openweather.org You can search any country of your choice from the web app and it will tell you the country tempeature, date, time, atmosphere changes. Having struggled understanding how to pass an API through this I learn a lot from my struggle.",
      linkname: "PrintriteNg",
      link1: "https://www.printrite.ng",
      datetitle: "May 2021 - Present",
      list1: "Did my internship program at Printrite Ng.",
      list2:
        "Work with languagues , platforms , frameworks, and content management systems such as PHP, VueJs, Github, Bitbucket, JavaScript, SQL and Figma.",
      list3:
        "Communicate with integrative teams of developers, engineers, designers and clients.",
    },
    {
      id: 2,
      title: "Dicemedia",
      title2: "--- Designer @",
      linkname: "Dicemediastudio",
      link: "https://www.printrite.ng",
      datetitle: "August 2019 - Present",
      list1: "I'm the Co-founder of Dicemedia Studio. ",
      list2:
        "I started my Graphic Designing journey back in 2019 down till date.",
      list3:
        "I'm well experienced with over 2 years experience and i can handle any graphic design jobs i have opportunity to get on to work with. I'm a team builder, working with teams has been my priority.",
    },
    {
      id: 3,
      title: "Lettads",
      title2: "--- Graphic Designer @",
      linkname: "Lettads",
      link3: "https://www.lettads.com.ng",
      datetitle: "Feb 2020 - Feb 2021",
      list1:
        "Designing layouts, producing images, and developing styles for websites, social media profiles.",
      list2:
        "Prioritizing workloads and coordinating multiple ongoing projects.",
      list3: "Implementing SEO and SEM tactics to get measurable results.",
    },
  ],
  data() {
    return {};
  },
};
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
  --focus-color-shadow: rgba(2, 12, 27, 0.7);
}

.button-style-1 {
  color: var(--color-focus);
  background-color: transparent;
  border: 1px dashed var(--color-focus-fam);
  border-radius: 0px 20px;
  padding: 1.25rem 1.88rem;
  word-spacing: 5px;
  width: 280px;
  height: 60px;
  line-height: 1;
  text-decoration: none;

  //Mobile Responsiveness
  @include breakpoint-down(medium) {
    width: 220px;
    height: 52px;
  }

  .heading-numbering > h2 {
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
    .button-style-2 {
      color: var(--color-focus);
      background-color: var(--color-focus);
      border-radius: 0px 20px;
      padding: 1.25rem 1.88rem;
      width: 93px;
      height: 61px;
      cursor: pointer;
      margin-top: -49px;
      margin-left: 157px;

      //Mobile Responsiveness
      @include breakpoint-down(medium) {
        margin-top: -42px;
        margin-left: 115px;
        width: 74px;
        height: 54px;
      }
    }
  }
}

.my-project {
  padding: 110px 11.944vw 0;

  @media (max-width: 575.98px) {
    padding: 60px 25px 0 27px;
  }

  @media (max-width: 767.98px) {
    padding: 60px 6.944vw 0;
  }

  .project {
    display: flex;
    align-items: center;
    position: relative;
    margin-bottom: 150px;

    .project-content {
      width: 100%;
      display: flex;
      justify-content: space-between;
      margin-right: -50px;
      position: relative;

      // &:nth-of-type(3n) {
      //   flex-direction: row-reverse;
      // }

      //Mobile Responsiveness
      @include breakpoint-down(medium) {
        flex-direction: column !important;
      }

      @media (max-width: 991.98px) {
        margin-right: -70px;
      }

      .image-container {
        background: var(--light-slate);
        padding: 25px;
        border-radius: 5px;
        width: 35.24vw;
        height: 35.24vw;

        @media (max-width: 991.98px) {
          padding: 20px;
        }

        @media (max-width: 1199.98px) {
          padding: 15px;
          width: 34.24vw;
          height: 34.24vw;
        }

        // come back here =============

        // @media (max-width: 1350px) {
        //   padding: 50px;
        // }

        // //Mobile Responsiveness
        // @include breakpoint-down(medium) {
        //   padding: 10px;
        //   width: 100%;
        //   height: unset;
        //   max-height: 450px;
        //   max-width: 450px;
        //   margin-bottom: 30px;
        // }

        @media (max-width: 767.98px) {
          padding: 25px;
          width: 100%;
          height: unset;
          max-height: 450px;
          max-width: 450px;
          margin-bottom: 30px;
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

        @media (max-width: 767.98px) {
          width: 100%;
        }

        h1 {
          color: #0db9ff;
          font-size: var(--fz-md);
          font-weight: 200;
          font-style: italic;
          line-height: 1.5;
          margin-bottom: 10px;
        }

        h3 {
          color: var(--light-slate);
          font-size: clamp(24px, 5vw, 28px);
          font-weight: 400px;
          margin-bottom: 20px;
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

          .stack {
            display: flex;
            width: 70px;
            height: 30px;
            justify-content: center;
            align-items: center;
            background: var(--color-focus);
            color: #112240;
            letter-spacing: 0.1em;
            font-size: 12px;
            border-radius: 4px;
            margin-right: 10px;
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
}
</style>