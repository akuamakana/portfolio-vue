<template>
  <div class="text-black sticky top-0 flex w-screen bg-white justify-center pt-10 z-50">
    <div class="flex justify-end w-3/4 items-center mb-6">
      <XyzTransitionGroup
        xyz="fade up-5 ease-out-back stagger"
        tag="div"
        class="flex items-center"
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
