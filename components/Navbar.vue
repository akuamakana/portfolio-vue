<template>
  <div
    id="app"
    class="font-sans antialiased w-screen flex justify-end sticky top-0 bg-white lg:justify-center"
  >
    <nav class="flex w-screen items-center justify-center flex-wrap p-6">
      <!-- Hide button on  -->
      <div class="block sm:hidden">
        <button
          class="flex items-center px-3 py-2 border rounded text-teal-300 border-teal-light hover:text-white hover:border-white"
          @click="open = !open"
        >
          <svg
            class="fill-current h-3 w-3"
            viewBox="0 0 20 20"
            xmlns="http://www.w3.org/2000/svg"
          >
            <title>Menu</title>
            <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
          </svg>
        </button>
      </div>
      <div
        :class="open ? 'block' : 'hidden'"
        class="w-full justify-end lg:mr-24 flex-grow sm:flex sm:items-center sm:w-auto"
      >
        <div class="flex flex-col md:hidden justify-end sm:flex-grow">
          <a
            v-scroll-to="{el: '#intro', offset: -200}"
            href="#"
            class="no-underline block mt-4 sm:inline-block sm:mt-0 hover:text-white mr-4"
          >
            Home
          </a>
          <a
            v-scroll-to="'#portfolio'"
            href="#"
            class="no-underline block mt-4 sm:inline-block sm:mt-0 hover:text-white"
          >
            Portfolio
          </a>          
          <a
            v-scroll-to="{el: '#resume', offset: -200}"
            href="#"
            class="no-underline block mt-4 sm:inline-block sm:mt-0 hover:text-white mr-4"
          >
            Resume
          </a>
          <a
            v-scroll-to="'#contact-me'"
            href="#"
            class="no-underline block mt-4 sm:inline-block sm:mt-0 hover:text-white"
          >
            Contact
          </a>
        </div>
        <XyzTransitionGroup
          xyz="fade up-5 ease-out-back stagger"
          tag="div"
          class="sm:flex items-center justify-center hidden"
        >
          <a
            v-if="isRendered"
            :key="1"
            v-scroll-to="{el: '#intro', offset: -200}"
            href="#"
            class="mx-8 text-xl text-gray-600"
          >
            Home
          </a>
          <a
            v-if="isRendered"
            :key="3"
            v-scroll-to="'#portfolio'"
            href="#"
            class="mx-8 text-xl text-gray-600"
          >
            Portfolio
          </a>
          <a
            v-if="isRendered"
            :key="2"
            v-scroll-to="{el: '#resume', offset: -200}"
            href="#"
            class="mx-8 text-xl text-gray-600"
          >
            Resume
          </a>
          <a
            v-if="isRendered"
            :key="4"
            v-scroll-to="'#contact-me'"
            href="#"
            class="ml-4 text-xl bg-green-400 rounded-lg py-3 text-white px-10 cursor-pointer"
          >
            Contact
          </a>
        </XyzTransitionGroup>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  data () {
    return {
      isRendered: false,
      open:false
    };
  },
  mounted() {
    this.isRendered = true;
  }
};
</script>
