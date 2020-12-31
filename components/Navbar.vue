<template>
  <div
    id="app"
    class="font-sans antialiased w-screen flex justify-end lg:justify-center"
  >
    <nav class="flex lg:w-3/4 items-center justify-center flex-wrap p-6">
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
        class="w-full justify-end flex-grow sm:flex sm:items-center sm:w-auto"
      >
        <div class="flex flex-col md:hidden justify-end sm:flex-grow">
          <a
            href="#responsive-header"
            class="no-underline block mt-4 sm:inline-block sm:mt-0 hover:text-white mr-4"
          >
            Home
          </a>
          <a
            href="#responsive-header"
            class="no-underline block mt-4 sm:inline-block sm:mt-0 hover:text-white mr-4"
          >
            Resume
          </a>
          <a
            href="#responsive-header"
            class="no-underline block mt-4 sm:inline-block sm:mt-0 hover:text-white"
          >
            Portfolio
          </a>          
          <a
            href="#responsive-header"
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
          <p
            v-if="isRendered"
            :key="1"
            class="mx-8 text-xl text-gray-600"
          >
            Home
          </p>
          <p
            v-if="isRendered"
            :key="2"
            class="mx-8 text-xl text-gray-600"
          >
            Resume
          </p>
          <p
            v-if="isRendered"
            :key="3"
            class="mx-8 text-xl text-gray-600"
          >
            Portfolio
          </p>
          <p
            v-if="isRendered"
            :key="4"
            class="ml-4 text-xl bg-green-400 rounded-lg py-3 text-white px-10 cursor-pointer"
          >
            Contact
          </p>
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
