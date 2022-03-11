<template>
  <section class="work-me">
    <div class="button-style">
      <h2 class="head-numbering">
        <span>02.</span> I’ve Worked here
        <div class="button-style2"></div>
      </h2>
    </div>

    <!-- Card here -->
    <div class="work-details">
      <div class="card_1"></div>
    </div>
    <router-view />
  </section>
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