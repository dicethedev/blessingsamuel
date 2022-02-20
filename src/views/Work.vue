<template>
  <section class="work-me">
    <div class="button-style">
      <h2 class="head-numbering">
        <span>02.</span> I’ve Worked here
        <div class="button-style2"></div>
      </h2>
    </div>

    <!-- Tabs behavior here -->
    <div class="work-details">
      <!-- I app a props name here called content and v-bind (:content) from tab.vue -->
      <Tab :content="tabData" />
      <!-- <TabsWrapper /> -->
    </div>
    <router-view />
  </section>
</template>

<script>
import Tab from "@/components/Tab.vue";
export default {
  components: {
    Tab,
  },
  data() {
    return {
      tabData: [
        {
          id: 1,
          title: "PrintriteNG",
          title2: "--- Intern Software Engineer @",
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
    };
  },
};
</script>

<style lang="scss">
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
  margin-top: 70px;
  margin-left: 380px;

  .button-style {
    color: var(--color-focus);
    background-color: transparent;
    border: 1px dashed var(--color-focus);
    border-radius: 10px 30px;
    padding: 1.25rem 1.88rem;
    word-spacing: 5px;
    width: 260px;
    height: 30px;
    line-height: 1;
    text-decoration: none;
    cursor: pointer;
    transition: var(--transition);

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
        margin-right: 2px;
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
      }
    }
  }
  .work-details {
    margin-top: 70px;
    display: flex;
    color: white;
    @media (min-width: 700px) {
      min-height: 340px;
    }
  }
}
</style>