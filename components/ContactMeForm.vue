<template>
  <form
    method="POST"
    data-netlify="true"
    class="flex flex-col flex-auto"
    data-netlify-honeypot="bot-field"
    name="contact-me"
  >
    <input
      type="hidden"
      name="form-name"
      value="contact-me"
    >
    <input
      class="my-4 p-2 border-gray-200 border-2 rounded-lg"
      type="text"
      name="name"
      placeholder="Name"
    >
    <input
      class="my-4 p-2 border-gray-200 border-2 rounded-lg"
      type="email"
      name="email"
      placeholder="Email"
    >
    <textarea
      class="my-4 p-2 border-gray-200 border-2 rounded-lg"
      rows="5"
      name="message"
      style="resize: none"
    />
    <button
      class="bg-green-400 p-3 rounded-lg mt-4 text-white focus:ring-0"
    >
      Send Message
    </button>
  </form>
</template>
