<template>
  <form
    class="flex flex-col"
    action=""
  >
    <input
      class="my-4 p-2 border-gray-200 border-2"
      type="text"
      placeholder="Name"
    >
    <input
      class="my-4 p-2 border-gray-200 border-2"
      type="text"
      placeholder="Email"
    >
    <input
      class="my-4 p-2 border-gray-200 border-2"
      type="text"
      placeholder="Subject"
    >
    <textarea
      class="my-4 p-2 border-gray-200 border-2"
      rows="5"
      style="resize: none"
    />
    <button
      class="bg-orange-400 p-3 rounded mt-4 focus:ring-0"
      type="button"
    >
      Send Message
    </button>
  </form>
</template>
