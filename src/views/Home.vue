<template>
  <div class="home-main">
    <div class="home-section">
      <div class="left">
         <h1>Hi, my name is</h1>
          <h2 class="big-heading">Blessing Samuel.</h2>
        <h3
          class="
            big-heading-2
            animate__animated animate__pulse"
        >
          The Tech guy with the Web.
        </h3>

          <p class="home-description">
            I love to build and style things that live on the web with great
            user interface & experience. I am very good with HTML5, CSS3 (SCSS
            included). I am also very good with JavaScript and its frameworks
            such as Vue.js & React. I have over 2 years professional experience in
            front end development.
          </p>
          <!-- Button link here -->
          <a class="email-link" href="#my-project">See Projects</a>
      </div>   
      <!-- <div class="right animate__animated animate__pulse animate__infinite">
        <img src="@/assets/Logo.svg" alt="">
      </div> -->
    </div>
    <div class="link-to-left">
      <ul class="style-left">
        <!-- Github link -->
        <li>
          <a
            href="https://github.com/dicethedev"
            target="_blank"
            rel="noreferrer"
          >
            <img src="@/assets/github.svg" alt="" />
          </a>
        </li>
        <!-- Twitter link -->
        <li>
          <a
            href="https://twitter.com/dicethedev"
            target="_blank"
            rel="noreferrer"
          >
            <img src="@/assets/twitter.svg" alt="" />
          </a>
        </li>
        <!-- Instagram link -->
        <li>
          <a href="https://www.instagram.com/dicethedev5/" target="_blank" rel="noreferrer">
            <img src="@/assets/instagram-fill.svg" alt="" />
          </a>
        </li>
        <!-- Linkedin link -->
        <li>
          <a
            href="https://www.linkedin.com/in/blessing-samuel-6a72b1211/"
            target="_blank"
            rel="noreferrer"
          >
            <img src="@/assets/linkedin.svg" alt="" />
          </a>
        </li>
        <!-- Line-focus bottom is here
        <img class="line-focus" src="@/assets/line-focus.svg" alt="" /> -->
      </ul>
    </div>
    <router-view />
  </div>

    <!-- cursor design -->
   <CustomCursor/>

  <!-- About me  -->
  <About />

  <!-- Project -->
  <Project />

  <!-- Experience me  -->
  <Experience />

  <!-- Skillset -->
  <SkillSet />

  <!-- Contact & Footer -->
  <Contact />


</template>

<script>
import CustomCursor from '@/components/CustomCursor.vue';
import About from '@/components/About.vue';
import Experience from '@/components/Experience.vue';
import Project from '@/components/Project.vue';
import SkillSet from '@/components/SkillSet.vue';
import Contact from '@/components/Contact.vue';
// @ is an alias to /src

export default {
  name: "Home",
  data() {
    return {
      show: true,
      email: "dicethedev@gmail.com",
    };
  },
  components: {
    About,
    Experience,
    Project,
    SkillSet,
    Contact,
    CustomCursor,
  },

  methods: {},
};
</script>

<style lang="scss">
@import "/src/scss/_mixins.scss";

.home-main {
width: 100%;
padding: 86px 14.944vw 0;
position: relative;
min-height: 711px;
display: flex;
align-items: center;


  @media (max-width: 575.98px) {
  padding: 114px 25px 0 27px;
  width: 100%;
   }

.home-section {
width: 100%;
display: flex;
flex-wrap: wrap;
justify-content: space-between;
align-items: center;
margin-right: -30px;

  @media (max-width: 991.98px){
  margin-right: 0;
}

//   @media (max-width: 1199.98px){
//   margin-right: -80px;
// }

.left {
  // width: 750px;
  // margin-right: 30px;

  //   @media (max-width: 767.98px){
  //   width: 440px;
  //   margin-right: 0;
  //   margin-top: 40px;
  //   }

  //   @media (max-width: 575.98px) {
  //   margin-top: 0;
  //   }

    h1 {
      margin: 0px 0px 30px 4px;
      color: var(--color-primary);
      word-spacing: 0.3125rem;
      font-size: clamp(13px, 5vw, 16px);
      font-weight: 400;

        @media (max-width: 480px){
          margin: 0px 0px 20px 2px;
       }
    }

    .big-heading {
        font-size: clamp(40px, 8vw, 70px);
        color: var(--lightest-slate);
        margin: 0;
      }
   
    .big-heading-2 {
     font-size: clamp(40px, 8vw, 70px);
     color: var(--darkest-slate);
     margin: 0;
     margin-top: 10px;
     line-height: 1;
    }

    .home-description{
     margin: 20px 0px 0px;
     max-width: 540px;
     line-height: 1.5;
     font-size: 1rem;
     margin-bottom: 50px;
     font-weight: 300;
     color: var(--darkest-slate);

     p:last-child,
     p:last-of-type {
        margin: 0px;
      }
    }

    .email-link {
        padding: 15px 25px;
        border: unset;
        border-radius: 0 20px;
        text-decoration: none;
        line-height: 1;
        background: var(--color-primary);
        position: relative;
        color: var(--light-slate);
        letter-spacing: 5px;
        text-transform: uppercase;
        cursor: pointer;
        word-spacing: 5px;
        font-weight: 400;
        transition: all 250ms ease-in-out;
        overflow: hidden;

        
       @media (max-width: 480px) {
         font-size: 14px;
       }

        &::before {
          content: "";
          position: absolute;
          top: 0;
          left: 0;
          height: 100%;
          width: 0;
          border-radius: 0 20px;
          background-color: var(--color-primary-variant);
          transition: all 250ms ease-in-out;
        }

        &:hover {
          color: #e8e8e8;
        }

        &:hover::before {
          width: 90%;
        }
      }
    }  
    
    // .right {
    //     position: relative;
    //     z-index: 1;
    //     width: 200px;
    //     height: 200px;
        
    //     img {
    //     object-fit: contain;
    //     width: 250px;
    //     max-height: 250px;

    //       // @media (max-width: 1199.98px){
    //       // width: 250px;
    //       //  max-height: 250px;
    //       //  }

    //     }
    //   }
}
  

.link-to-left {
  width: 40px;
  position: fixed;
  bottom: 0px;
  left: 40px;
  right: auto;
  z-index: 10;
  transition: var(--transition);
  transition: var(--easing);

    @media (max-width: 1080px) {
     left: 20px;
     right: auto;
    }

  ul,
  .style-left {
    display: flex;
    flex-direction: column;
    -webkit-box-align: center;
    align-items: center;
    margin: 0px;
    padding: 0px;
    list-style: none;

    //the line below social 
    &::after {
    content: "";
    display: block;
    width: 1px;
    height: 90px;
    margin: 0px auto;
    background: var(--darkest-slate);
    }
  }

  li {
    display: list-item;
    text-align: -webkit-match-parent;
  }

  li a {
    padding: 15px;
  }

  a {
    display: inline-block;
    text-decoration: none;
    text-decoration-skip-ink: auto;
    color: inherit;
    position: relative;
    transition: var(--transition);
  }

  li a img {
    width: 20px;
    height: 20px;
    transition: var(--transition);
    animation-delay: var(--easing);

    &:hover {
      border: 1px dashed var(--color-primary);
      padding: 5px;
      border-radius: 8px;
    }
  }

  // Line-focus styling area is here
  // .line-focus {
  //   width: 1.8px;
  //   position: fixed;
  //   bottom: 0px;
  //   right: auto;
  //   z-index: 10;

  //   img {
  //     margin-right: -35px;
  //   }
  // }


  //Mobile Responsiveness
  @include breakpoint-down(small) {
    display: none;
  }

  //Mobile Responsiveness
  @include breakpoint-down(medium) {
    display: none;
  }

}

}

//link-to-right styling area
// .link-to-right {
//   display: flex;
//   flex-direction: column;
//   -webkit-box-align: center;
//   align-items: center;
//   position: fixed;
//   margin-left: 2rem;

//   a {
//     display: inline-block;
//     margin: 20px auto;
//     padding: 10px;
//     margin-left: 120px;
//     margin-top: -205px;
//     font-size: 12px;
//     font-weight: 400;
//     line-height: 18px;
//     letter-spacing: 0.1em;
//     -webkit-writing-mode: vertical-rl;
//     writing-mode: vertical-rl;
//     text-decoration: none;
//     text-decoration-skip-ink: auto;
//     color: #8892b0;
//     transition: var(--transition);

//     &:hover {
//       border: 1px dashed #00cffd;
//       color: #00cffd;
//     }
//   }

//   ul,
//   .style-right {
//     // display: flex;
//     flex-direction: column;
//     -webkit-box-align: center;
//     align-items: center;
//     margin: 0px;
//     padding: 0px;
//     list-style: none;
//     margin-top: 200px;
//     // Margining it to right is right here
//     margin-left: 120px;
//   }

//   // focus-line styling area is here
//   .focus-line {
//     width: 1.8px;
//     position: fixed;
//     bottom: 0px;
//     right: auto;
//     z-index: 10;
//   }
//   //Mobile Responsiveness
//   @include breakpoint-down(small) {
//     display: none;
//   }
//   //Responsiveness for Desktop or Laptop
//   @include breakpoint-down(medium) {
//     display: none;
//   }

//   //Responsiveness for Desktop or Laptop
//   @include breakpoint-down(large) {
//     display: none;
//   }
// }
</style>