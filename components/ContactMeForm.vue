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
      name="contact-me"
      value="contact-me"
    >
    <input
      v-model="form.name"
      class="my-4 p-2 border-gray-200 border-2 rounded-lg"
      type="text"
      name="name"
      placeholder="Name"
    >
    <input
      v-model="form.email"
      class="my-4 p-2 border-gray-200 border-2 rounded-lg"
      type="email"
      name="email"
      placeholder="Email"
    >
    <textarea
      v-model="form.message"
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

<script>
import axios from 'axios';
export default {
  data: () => ({
    form: {
      name: '',
      email: '',
      message: ''
    }
  }),
  methods: {
    resetForm() {
      this.$set(this.form, 'name', '');
      this.$set(this.form, 'email', '');
      this.$set(this.form, 'message', '');
    },
    encode(data) {
      return Object.keys(data)
        .map(
          (key) => `${encodeURIComponent(key)}=${encodeURIComponent(data[key])}`
        )
        .join('&');
    },
    handleSubmit() {
      const axiosConfig = {
        header: { 'Content-Type': 'application/x-www-form-urlencoded' }
      };
      axios.post(
        '/',
        this.encode({
          'form-name': 'contact-me',
          ...this.form
        }),
        axiosConfig
      );
      this.resetForm();
    }
  }
};
</script>
