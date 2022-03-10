<template>
  <section class="project-me">
    <div class="button-style">
      <h2 class="head-numbering">
        <span>03.</span> I’ve Built this
        <div class="button-style2"></div>
      </h2>
    </div>

    <div class="wrapper-grid"></div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
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

.project-me {
  position: relative;
  height: 100vh;
  visibility: visible;
  opacity: 1;
  transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
  transition: opacity 0.5s cubic-bezier(0.645, 0.045, 0.355, 1) 0.2s,
    transform 0.5s cubic-bezier(0.645, 0.045, 0.355, 1) 0.2s;
  margin-top: 10px;
  margin-left: 380px;

  .button-style {
    color: var(--color-focus);
    background-color: transparent;
    border: 1px dashed var(--color-focus);
    border-radius: 10px 30px;
    padding: 1.25rem 1.88rem;
    word-spacing: 5px;
    width: 230px;
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
      visibility: visible;
      //  opacity: 1;
      //  transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
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
        margin-left: 160px;
      }
    }
  }

  .wrapper-grid {
    display: grid;
    grid-template-columns: repeat(3, 2fr);
    gap: 20px;
    margin-left: -70px;
    //     justify-content: center;

    .project-container {
      overflow: hidden;
      box-shadow: 0px 2px 8px 0px var(--color-focus);
      background-color: #16294b;
      text-align: center;
      border-radius: 1rem;
      position: relative;
      //  margin: 0.1rem;
      width: 280px;
      height: 500px;
      margin-top: 60px;
    }

    .project-img {
      position: absolute;
      //  The weather screen shot image is in the background-image
      background-image: url("../assets/screen.jpg");
      height: 6rem;
      width: 100%;
      background-position: center;
      background-repeat: no-repeat;
      background-size: cover;
    }

    //The Imge-cliping is here below
    .banner-img {
      width: 8rem;
      clip-path: circle(0px at center);
      margin-top: 70px;
    }

    h1 {
      color: #8993b1;
      font-size: 1.2rem;
      top: 50px;
    }
    //h1
    .project-overline {
      font-style: italic;
      font-weight: 100;
      font-size: 14px;
      // line-height: 10px;
      color: #00cffd;
    }
    .description-container {
      display: flex;
      position: relative;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      background-color: #16294b;
      box-shadow: 4px 7px 57px 2px rgba(0, 0, 0, 0.25);
      border-radius: 20px;
      padding: 1.5rem;
      width: 220px;
      height: 140px;
      transform: translate(23%-20%);
      //p
      .description {
        //  position: absolute;
        margin: 1rem 0.5rem;
        font-size: 13.5px;
        color: #8993b1;
      }
    }
    //ul
    .project-tech-list {
      display: flex;
      flex-wrap: wrap;
      position: relative;
      z-index: 2;
      margin: 10px 0px 10px 90px;
      padding: 0px;
      list-style: none;
      color: #8993b1;

      li {
        margin-top: 10px;
        margin-right: 10px;
      }
    }

    .project-links {
      display: flex;
      -webkit-box-align: center;
      align-items: center;
      position: relative;
      margin-top: 10px;
      margin-left: 10px;
      margin-bottom: 10px;

      a {
        margin-left: 20px;
        img {
          width: 21.3px;
          height: 21.3px;
          transition: var(--transition);
          transition: var(--easing);

          &:hover {
            border: 1px dashed #00cffd;
            padding: 5px;
          }
        }
      }
    }
  }
}
</style>