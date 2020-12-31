<template>
  <div class="w-screen flex justify-center items-center">
    <div class="h-screen w-screen grid grid-cols-6 grid-rows-2 pt-20">
      <!-- <div class="col-span-1 social flex flex-row-reverse items-center justify-end"> -->
      <XyzTransitionGroup
        xyz="fade left-5 ease-out-back stagger delay-10"
        class="col-span-1 col-start-1 social flex flex-row-reverse items-start justify-end"
      >
        <p
          v-if="isRendered"
          :key="1"
          class="transform rotate-180 border rounded border-green-400 px-2 py-5 my-8"
        >
          LinkedIn
        </p>
        <p
          v-if="isRendered"
          :key="2"
          class="transform rotate-180 border rounded border-green-400 px-2 py-5 my-8"
        >
          Github
        </p>
        <p
          v-if="isRendered"
          :key="3"
          class="transform rotate-180 border rounded border-green-400 px-2 py-5 mb-8 mt-24"
        >
          Email
        </p>
      </XyzTransitionGroup>
      <!-- </div> -->
      <XyzTransition
        appear
        xyz="fade delay-25"
      >
        <div class="flex flex-col col-start-2 ml-32 col-span-5">
          <h1 class="header leading-none">
            I'm <span class="text-green-400">
              Kion Kaimi
            </span>
          </h1>
          <h3 class="text-xl text-gray-600">
            Web Developer // Software Engineer
          </h3>
        </div>
      </XyzTransition>
      <svg
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 1440 320"
        class="col-span-6 h-full"
      >
        <path
          fill="#68D391"
          fill-opacity="0.8"
          d="M0,256L60,229.3C120,203,240,149,360,154.7C480,160,600,224,720,213.3C840,203,960,117,1080,117.3C1200,117,1320,203,1380,245.3L1440,288L1440,320L1380,320C1320,320,1200,320,1080,320C960,320,840,320,720,320C600,320,480,320,360,320C240,320,120,320,60,320L0,320Z"
        />
        <path
          fill="#68D391"
          fill-opacity="0.6"
          d="M0,256L60,261.3C120,267,240,277,360,250.7C480,224,600,160,720,160C840,160,960,224,1080,213.3C1200,203,1320,117,1380,74.7L1440,32L1440,320L1380,320C1320,320,1200,320,1080,320C960,320,840,320,720,320C600,320,480,320,360,320C240,320,120,320,60,320L0,320Z"
        />
      </svg>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      isRendered: false
    };
  },
  mounted() {
    this.isRendered = true;
  }
};
</script>


<style scoped>
  .social {
    writing-mode: tb-rl;
  }
  .header {
    font-size: 6rem;
  }

</style>
