<template>
  <div
    class="
      button-style-1
      container
      animate__animated animate__bounce animate__infinite
    "
  >
    <h2 class="heading-numbering">
      <span>02.</span> I’ve Built this
      <div class="button-style-2"></div>
    </h2>
  </div>

  <div class="my-project" id="my-project">
    <div  class="projects">
      <div class="project-content">
        <div class="image-content">
         <a href="https://invoice-app-gray.vercel.app/" target="_blank" rel="noreferrer"><img src="../assets/project-image-2.jpg" alt=""></a> 
        </div>
         <div class="project-details">
           <h3>Featured Project</h3>
           <h1>Invoice App</h1>
            <p>A Full stack Invoice Application crafted using Vuejs(vuex) & Firebase (firebase).
              It keep track records of all invoices that is created.
              It Features include Create, Edit, Delete, Mark as Paid/Pending and also you can print
              the invoice. I Learned how to use the Vuex effective, how firebase cloud data work efficiently 
              and how to handle promises, fetch/axios data from a 3rd party API, and I make use of limited 
              NPM packages. You can check it and see how it works and it is open for everyone
              to see and feel the environment on the application.
            </p>

               <div class="tech-stacks">
                 <div class="stack">HTML</div>
                  <div class="stack">CSS</div>
                  <div class="stack">VUE.JS</div>
                  <div class="stack">FIREBASE</div>
                   <div class="stack">VERCEL</div>
               </div>

                <div class="project-link">
               <a href="https://github.com/dicethedev/invoice-app" target="_blank" rel="noreferrer">
              <img src="../assets/akar-icons_github-fill.svg" alt="github" />
              </a>
            <a href="https://invoice-app-gray.vercel.app/" target="_blank" rel="noreferrer">
              <img
                src="../assets/bi_arrow-right-circle-fill.svg"
                alt="arrow-right"
              />
            </a>
                 </div>
         </div>
      </div>
    </div>

     <div  class="projects">
      <div class="project-content">
        <div class="image-content">
         <a href="https://diceflix.netlify.app/" target="_blank" rel="noreferrer">
         <img src="../assets/project-image-3.jpg" alt=""></a> 
        </div>
         <div class="project-details">
           <h3>Featured Project</h3>
           <h1>Diceflix</h1>
            <p>Diceflix is movie search engine. I called it Diceflix because the name inspiration
            comes from Netflix. This project was built with React.js and with the help of OMDb API.
            You search any movie of your choices and it will display 
            the movie image, year, title and 
            date possibly.</p>

               <div class="tech-stacks">
                 <div class="stack">HTML</div>
                  <div class="stack">CSS</div>
                  <div class="stack">REACT</div>
                  <div class="stack">OMDbAPI</div>
                   <div class="stack">NETLIFY</div>
               </div>

                <div class="project-link">
               <a href="https://github.com/dicethedev/diceflix-react" target="_blank" rel="noreferrer">
              <img src="../assets/akar-icons_github-fill.svg" alt="github" />
              </a>
            <a href="https://diceflix.netlify.app/" target="_blank" rel="noreferrer">
              <img
                src="../assets/bi_arrow-right-circle-fill.svg"
                alt="arrow-right"
              />
            </a>
                 </div>
         </div>
      </div>
    </div>

     <div  class="projects">
      <div class="project-content">
        <div class="image-content">
         <a href="https://weatherapp-blessing-samuel.vercel.app/" target="_blank" rel="noreferrer"><img src="../assets/project-image-1.jpg" alt=""></a> 
        </div>
         <div class="project-details">
           <h3>Featured Project</h3>
           <h1>Weather App</h1>
            <p>Weather app develop with Vue. An API is pass from openweather.org 
              You can search any country of your choice from the web app and it will 
              tell you the country tempeature, date, time, atmosphere changes. 
              Having struggled understanding how to pass an API through this I learn a lot from
               my struggle.</p>

               <div class="tech-stacks">
                 <div class="stack">HTML</div>
                  <div class="stack">CSS</div>
                  <div class="stack">VUE.JS</div>
                  <div class="stack">API</div>
                   <div class="stack">VERCEL</div>
               </div>

                <div class="project-link">
               <a href="https://github.com/dicethedev/Weatherapp" target="_blank" rel="noreferrer">
              <img src="../assets/akar-icons_github-fill.svg" alt="github" />
              </a>
            <a href="https://invoice-app-gray.vercel.app/" target="_blank" rel="noreferrer">
              <img
                src="../assets/bi_arrow-right-circle-fill.svg"
                alt="arrow-right"
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
  props: {
   content: Array
  },
  data() {
    return {
    };
  },
};
</script>

<style lang="scss">
@import "/src/scss/_mixins.scss";

.button-style-1 {
  background-color: transparent;
  border: 1px dashed var(--color-primary);
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
    .button-style-2 {
      background-color: var(--color-primary);
      border-radius: 0px 20px;
      padding: 1.25rem 1.88rem;
      width: 93px;
      height: 61px;
      cursor: pointer;
      margin-top: -49px;
      margin-left: 157px;

      //Mobile Responsiveness
      @include breakpoint-down(medium) {
        margin-top: -41px;
        margin-left: 118px;
        width: 73px;
        height: 55px;
      }
    }
  }
}

.my-project {
    margin-top: 87px;
    padding: 110px 10.944vw 0;

    @media (max-width: 767.98px) {
    padding: 60px 8.944vw 0;
  }

.projects {
    display: flex;
    align-items: center;
    margin-bottom: 200px;
    position: relative;

    @media (max-width: 991.98px) {
    margin-bottom: 120px;
    }

    @media (max-width: 1199.98px) {
     margin-bottom: 150px;
    }

.project-content {
    width: 100%;
    display: flex;
    justify-content: space-between;
    margin-right: -50px;
    position: relative;
    z-index: 1;


    // &:nth-last-of-type(2n) {
    //   flex-direction: row-reverse;
    // }

    
     //Mobile Responsiveness
    @include breakpoint-down(medium) {
        flex-direction: column !important;
    }


    @media (max-width: 991.98px) {
        margin-right: -70px;
    }

.image-content {
    background: var( --color-primary-variant);
    padding: 25px;
    // box-shadow: 0 12px 30px rgba(50 224 196 / 5%);
    border-radius: 5px;
    width: 35.24vw;
    height: 35.24vw;

    &:nth-of-type(2n) {
        flex-direction: row-reverse;
    }


     @media (max-width: 767.98px) {
        padding: 25px;
        width: 100%;
        height: unset;
        max-height: 500px;
        max-width: 500px;
        margin-bottom: 30px;
     }

      @media (max-width: 991.98px) {
         padding: 20px;
     }
     
   img {
    object-fit: cover;
    object-position: left center;
    width: 100%;
    height: 100%;
    border-radius: 4px;
    }

}

.project-details {
     width: 36vw;

  @media (max-width: 767.98px) {
    width: 100%;
  }

    h3 {
      font-size: 16px;
      color: var(--color-primary);
      font-style: italic;
      line-height: 1.71;
      font-weight: 400;

      @media (max-width: 424.98px) {
      font-size: 14px;
     }
}
     
    h1 {
    font-size: 38px;
    line-height: 1.71;
    margin-bottom: 10px;
    color: var(--lightest-slate);

    @media (max-width: 575.98px){
    font-size: 25px;
   }
}

    p {
     font-size: 16px;
     line-height: 1.53;
     font-weight: 300;
     color: var(--darkest-slate);

     @media (max-width: 424.98px) {
      font-size: 14px;
    }
}

    .tech-stacks {
     display: flex;
     margin-top: 30px;
     margin-bottom: 15px;
     
     .stack {
      // width: 98px;
      // height: 36px;
      display: flex;
      justify-content: center;
      align-items: center;
      // background: rgba(var(--primary-rgb-color),.1);
      color: var(--color-primary);
      border-radius: 5px;
      margin-right: 20px;
      letter-spacing: .2em;
      font-size: 12px;

       @media (max-width: 480px) {
         font-size: 10px;
       }
     }          
  }
    
    .project-link {
          display: flex;
          margin-top: 20px;

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
                // border: 1px dashed #00cffd;
                // color: var(--primary-color);
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