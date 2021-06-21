<template>
  <div id="app">
    <div style="margin-top: 200px; margin-left: 200px">
      <button class="btn btn-btn-primary" @click="show = !show">Toggle</button>

      <!-- <transition
        enter-active-class="animate__animated animate__pulse slow"
        leave-active-class="animate__animated animate__zoomOut"
        name="fade"
      >
        <p v-if="show" style="width: 200px;">Lorem ipsum dolor sit amet</p>
      </transition> -->
       <!-- <transition name="fade">
        <p v-if="show" style="width: 200px;">Lorem ipsum dolor sit amet</p>
      </transition>

      <transition name="pulse-fade" type="animation">
        <p v-if="show" style="width: 200px;">Lorem ipsum dolor sit amet</p>
      </transition> -->

      <transition name="fade" mode="out-in" appear="">
        <p v-if="show" key="lorem">Lorem ipsum dolor sit amet</p>
        <p v-else key="ipsum">Nothing to show here</p>
      </transition>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'app',
    data() {
      return {
        show: true
      }
    }
  }
</script>

<style>
  /* .fade-enter {
    opacity: 0;
  }

  .fade-enter-active, .fade-leave-active {
    transition: opacity 0.2s;
  }

  .fade-leave-to {
    opacity: 0;
  }

  .slow {
    animation-duration: 2s;
  } */
/*
  .v-enter-active {
    animation: pulse 0.5s;
  }

  .v-leave-active {
    animation: fade-out 0.5s;
  } */

  /* .fade-enter, .fade-leave-to, .pulse-fade-enter, .pulse-fade-leave-to {
    opacity: 0;
  }

  .fade-enter-active, .fade-leave-active {
    transition: opacity 1;
  }

  .pulse-fade-enter-active {
    transition: opacity 0.5s;
    animation: pulse 1s;
  }

  .pulse-fade-leave {
    opacity: 1;
  }

  .pulse-fade-leave-active {
    transition: opacity 1s;
    animation: pulse 1s;
  } */

  /* @keyframes pulse {
    from {
      transform: scale3d(1, 1, 1);
    }

    50% {
      transform: scale3d(1.2, 1.2, 1.2);
    }

    to {
      transform: scale3d(1, 1, 1);
    }

     from {
      opacity: 0;
      transition: opacity;
    }

    to {
      opacity: 1;
    }
  }

  @keyframes fade-out {
    from {
      opacity: 1;
      transition: opacity;
    }

    to {
      opacity: 0;
    }
  } */

  .fade-enter, .fade-leave-to {
    opacity: 0;
  }

  .fade-enter-active, .fade-leave-active {
    transition: opacity 1s;
  }
</style>
