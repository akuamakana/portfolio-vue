<template>
  <div class="w-screen flex justify-center items-center">
    <div class="h-screen w-screen flex flex-col px-4 lg:grid lg:grid-cols-6 grid-rows-2 lg:pt-20">
      <XyzTransitionGroup
        xyz="fade ease-out-back left-5 stagger delay-10"
        class="col-span-1 col-start-1 social hidden lg:flex flex-row-reverse items-start justify-end"
      >
        <p
          v-if="isRendered"
          :key="1"
          class="cursor-pointer transform rotate-180 border rounded border-green-400 px-2 py-5 my-8"
        >
          LinkedIn
        </p>
        <p
          v-if="isRendered"
          :key="2"
          class="cursor-pointer transform rotate-180 border rounded border-green-400 px-2 py-5 my-8"
        >
          Github
        </p>
        <p
          v-if="isRendered"
          :key="3"
          class="cursor-pointer transform rotate-180 border rounded border-green-400 px-2 py-5 mb-8 mt-24"
        >
          Email
        </p>
      </XyzTransitionGroup>
      <XyzTransition
        appear
        xyz="fade"
        class=""
      >
        <div class="flex flex-col lg:col-start-2 lg:ml-32 col-span-4">
          <div>
            <h1 class="lg:header mobile-header leading-none">
              I'm <span class="text-green-400">
                Kion Kaimi
              </span>
            </h1>
            <h3 class="text-xl text-gray-600">
              Web Developer // Software Engineer
            </h3>
          </div>
          <XyzTransitionGroup
            xyz="fade ease-out-back up-5 stagger delay-5"
            class="grid grid-cols-3 gap-6 lg:hidden mb-12"
          >
            <p
              v-if="isRendered"
              :key="1"
              class="cursor-pointer border rounded border-green-400 py-2 mt-8 text-center"
            >
              LinkedIn
            </p>
            <p
              v-if="isRendered"
              :key="2"
              class="cursor-pointer border rounded border-green-400 py-2 mt-8 text-center"
            >
              Github
            </p>
            <p
              v-if="isRendered"
              :key="3"
              class="cursor-pointer border rounded border-green-400 py-2 mt-8 text-center"
            >
              Email
            </p>
          </XyzTransitionGroup>
          <div class="lg:mt-24 lg:pt-24">
            <p class="leading-relaxed mb-6 text-lg text-gray-600">
              Lorem ipsum dolor sit amet consectetur, adipisicing elit. Eveniet modi ea excepturi eum? Ipsam atque enim vel, consectetur ipsum ipsa obcaecati. Modi natus nulla voluptatibus, in est facilis molestiae iure optio vel quidem quisquam mollitia magnam fugiat assumenda aliquam eum, molestias minima ipsum iusto! Quae ut tempore labore! Suscipit ipsum dignissimos veniam omnis nulla inventore laborum ex repudiandae eos modi, voluptatibus provident et esse dolore necessitatibus doloribus animi dolores quod atque quo cum! Nisi nesciunt aperiam, odio rem incidunt voluptate!
            </p>
            <button class="text-xl bg-green-400 rounded-lg py-3 text-white px-10 cursor-pointer">
              Download CV
            </button>
          </div>
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
import { hideAt } from 'vue-breakpoints';
export default {
  components: hideAt,
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
  .mobile-header {
    font-size: 5rem;
  }

</style>
