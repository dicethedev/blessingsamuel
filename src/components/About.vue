<template>
  <div class="about-me" id="about-me">
    <div class="about-me-content">
      <div class="left">
        <div
          class="
            container
            button-style-1
            animate__animated animate__bounce"
        >
          <h2 class="head-numbering">
            <span>01.</span>About Me
            <div class="button-style-2"></div>
          </h2>
        </div>

       <div class="right">
          <img class="about-me-img" src="@/assets/Profile.jpg" alt="" />
        </div>

        <p class="about-paragraph">
          I am a Frontend Software Engineer currently based in Nigeria.
          I love programming and designing things that live on the web. 
          My interest is web development  and my web development  journey started 
          back then in 2020 when I decided  to try to work on a free HTML template. 
          I am very adept using Javascript and its Frameworks like Vue & React. 
          I can work with zeal and real wizardy.
          I want to learn New things, because that's what brings joy to my life Up.
          I believe in team success & growth, however I always put my best & maintain a strong
          team bonding for every project I get to work on. 
        </p>
        <p class="about-paragraph">
          I was born in Kogi State, Nigeria. I graduated with a second class
          upper division in Software Engineering in Nigeria. My love
          for arithmetic and logic brought me towards the path of software
          development. I look forward to expanding my dexterity in the blockchain
          development space.
        </p>
        <!-- <p>Here are a few technologies l’ve been working with recently:</p> -->
      </div>
    </div>
  </div>
  <router-view />
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "/src/scss/_mixins.scss";

.about-me {
  width: 100%;
  display: flex;
  align-items: center;
  padding: 200px 15.944vw 150px;
  overflow-y: hidden;
  position: relative;
  margin-top: -50px;

  .about-me-content {
    width: 100%;
    margin-right: -50px;

    .left {
      .button-style-1 {
        // color: var( --color-primary-variant);
        background-color: transparent;
        border: 1px dashed var( --color-primary);
        border-radius: 0px 20px;
        padding: 1.25rem 1.88rem;
        word-spacing: 5px;
        width: 220px;
        height: 60px;
        line-height: 1;
        text-decoration: none;
        margin-bottom: 70px;

        //Mobile Responsiveness
        @include breakpoint-down(medium) {
          width: 190px;
          height: 52px;
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
          font-size: 25px;
          font-weight: 700;
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
            margin-right: 10px;

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
            width: 75px;
            height: 60px;
            cursor: pointer;
            margin-top: -48px;
            margin-left: 115px;

            //Mobile Responsiveness
            @include breakpoint-down(medium) {
              margin-top: -42px;
              margin-left: 90px;
              width: 69px;
              height: 56px;
            }
          }
        }
      }
    }

    .right {
      float: right;
      width: 44.7%;
      margin-left: 5.5%;
      margin-bottom: 30px;

      @media (max-width: 424.98px) {
        float: none;
        width: 100%;
        height: 400px;
        margin: 30px 0;
      }

       img {
        position: relative;
        border-radius: 3px;
        object-position: top center;
        max-height: 540px;
        box-shadow: 0px 9px 57px -11px var(--color-primary);
      }
      .about-me-img {
        width: 100%;
        height: 100%;
        object-fit: cover;
      }

    }

    .about-paragraph {
      font-size: 18px;
      line-height: 2;
      color: var(--darkest-slate);
      font-weight: 200;
      margin-bottom: 46px;

      @media (max-width: 767.98px) {
        font-size: 16px;
        line-height: 1.7;
        margin-bottom: 32px;
      }

      @media (max-width: 424.98px) {
        font-size: 14px;

      }
    }
  }
}

// @import "../assets/styles/_mixings-method.scss";
</style>

