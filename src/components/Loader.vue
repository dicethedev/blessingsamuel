<template>
  <transition name="fade">
    <!-- //changing to v-if directive (v-if="show")  -->
    <!-- <div class="preloader"> -->
    <div v-if="show" class="preloader">
      <div class="container-space">
        <div class="logo">
          <img src="@/assets/Logo.svg" alt="" />
        </div>
        <!-- <p>Blessing Samuel Project!</p> -->
        <div class="circles">
          <div class="circle"></div>
          <div class="circle"></div>
          <div class="circle"></div>
        </div>
      </div>
    </div>
  </transition>
</template>

<script>
//changing the if directive
export default {
  name: "loader",
  data() {
    return {
      show: true,
    };
  },

  mounted() {
    this.showToggle();
  },

  methods: {
    //setting the animation to delay to let application load
    showToggle() {
      setTimeout(() => {
        this.show = false;
      }, 1000);
    },
  },
};
</script>

<style lang="scss">
//Preloader must fill full window and hide background till the load ends
.preloader {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  position: fixed;
  width: 100%;
  height: 100%;
  transition: opacity 200ms linear;
  background-color: var(--color-loader);
  z-index: 10002;
  overflow: hidden;

  .container-space {
    width: 115px;
    height: 115px;
    background: #ebebeb;
    border-radius: 30px;
    padding: 30px 25px;
    margin-bottom: 40px;

    .logo img {
      width: 6rem;
      height: 6rem;
      background-repeat: no-repeat;
      margin-left: -14px;
      margin-top: -25px;
    }

    .circles {
      display: flex;
      margin-top: -15px;
      margin-left: 6px;

      .circle {
        width: 10px;
        height: 10px;
        margin: 5px;
        background: var(--color-linear-gradient);
        border-radius: 50%;
        animation-name: scaleIn;
        animation-duration: 1s;
        transform: scale(0);

        &:nth-child(1) {
          animation-delay: 0s;
        }
        &:nth-child(2) {
          animation-delay: 0.1s;
        }
        &:nth-child(3) {
          animation-delay: 0.2s;
        }
        //    &:nth-child(4) {
        //      animation-delay: 0.3s;
        //    }
        //    &:nth-child(5) {
        //      animation-delay: 0.4s;
        //    }
      }
    }
  }

  .fade-enter-active,
  .fade-leave-active {
    transition: opacity 1s;

    .logo {
      animation-name: scaleOut;
      animation-duration: 1s;
      p {
        animation-name: scaleOut;
        animation-duration: 1s;
      }
    }
  }

  
  .fade-enter,
  .fade-leave-to {
    opacity: 0;
  }

  @keyframes scaleOut {
    0% {
      transform: scale(1);
    }
    100% {
      transform: scale(0);
    }
  }

  @keyframes scaleIn {
    0% {
      transform: scale(0);
    }
    100% {
      transform: scale(1);
    }
  }
}
</style>