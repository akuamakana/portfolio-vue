<template>
  <form
    class="flex flex-col"
    action=""
  >
    <input
      class="my-4 p-2 border-gray-200 border-2 rounded-lg"
      type="text"
      placeholder="Name"
    >
    <input
      class="my-4 p-2 border-gray-200 border-2 rounded-lg"
      type="text"
      placeholder="Email"
    >
    <input
      class="my-4 p-2 border-gray-200 border-2 rounded-lg"
      type="text"
      placeholder="Subject"
    >
    <textarea
      class="my-4 p-2 border-gray-200 border-2 rounded-lg"
      rows="5"
      style="resize: none"
    />
    <button
      class="bg-green-400 p-3 rounded-lg mt-4 focus:ring-0"
      type="button"
    >
      Send Message
    </button>
  </form>
</template>
