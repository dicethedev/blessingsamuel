<template>
  <!-- This when you are passing props -->
  <!-- {{ content }} check readme.txt -->
  <div>
    <!-- 1  add click event below and a bind class is there also :class="{ '': current == 1 }" I will use this later -->

    <button
      @click="selectTab(info.id)"
      v-for="info in content"
      :key="info"
      class="work-places"
    >
      <h1>{{ info.title }}</h1>
    </button>

    <!-- First Container -->
    <!-- Added a v-if directive here -->
    <template v-for="info in content" :key="info">
      <div v-if="currentTab == info.id" class="container">
        <h2>
          <span>{{ info.title }}</span> {{ info.title2 }}
          <a href="https://www.printrite.ng" target="_blank" rel="noreferrer"
            >{{ info.linkname }}
          </a>
        </h2>
        <h3>{{ info.datetitle }}</h3>
        <ul>
          <li>{{ info.list1 }}</li>
          <li>
            {{ info.list2 }}
          </li>
          <li>
            {{ info.list3 }}
          </li>
        </ul>
      </div>
    </template>
  </div>
</template>
//For Tab setting
// tabData: [
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
<script>
export default {
  props: {
    // msg: String,
    content: Array,
  },
  data() {
    return {
      currentTab: 1,
    };
  },
  methods: {
    selectTab(selectedTab) {
      this.currentTab = selectedTab;
    },
  },
};
</script>

<style lang="scss" scoped>
:root {
  --color-focus: #00cffd;
  --color-light: #ebebeb;
  --fz-sm: 13px;
  --fz-md: 18px;
  --fz-heading: 32px;
  --lightest-slate: #ccd6f6;
  --easing: cubic-bezier(0.645, 0.045, 0.355, 1);
  --transition: all 0.25s cubic-bezier(0.645, 0.045, 0.355, 1);
}

button,
.work-places {
  background-color: transparent;
  border: 1px solid #00cffd;
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  cursor: pointer;

  h1 {
    color: #00cffd;
    font-size: 16px;
    margin: 1px;
    font-weight: 400;
    // &:hover {
    //   color: #fff;
    // }
  }
}

button {
  margin-right: 30px;
  &:hover {
    color: #fff;
    background-color: #00cffd;
    transition: var(--transition);
  }
  h1 {
    &:hover {
      color: #ebebeb;
    }
  }
}

.container {
  position: absolute;
  display: flex;
  background: var(--color-focus);
  width: 40rem;
  margin-top: 10px;
  margin-left: 3px;

  h2 {
    position: absolute;
    display: flex;
    margin-top: -58px;
    margin-right: -10px;
    font-size: 20px;
    font-style: italic;
    color: #112240;
    span {
      margin-top: 2px;
      margin-right: 5px;
      font-size: 18px;
      font-weight: 400;
    }

    a {
      color: #ebebeb;
      display: inline-block;
      text-decoration: none;
      text-decoration-skip-ink: auto;
      transition: var(--transition);
      margin-left: 5px;

      &:hover {
        border: 1px dashed #112240;
        color: #112240;
        padding: 2px;
      }
    }
  }

  h3 {
    position: absolute;
    font-size: 18px;
    margin-top: -30px;
    font-weight: 400;
    color: #ebebeb;
  }

  ul {
    color: #112240;
    list-style: none;
    line-height: 25px;
    li::before {
      content: "► ";
      color: #ebebeb;
    }
  }
}
</style>