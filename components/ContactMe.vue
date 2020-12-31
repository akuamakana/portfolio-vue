<template>
  <div class="flex flex-col w-screen justify-center lg:items-center py-8">
    <div class="lg:w-3/4 flex-auto px-4 lg:flex-none lg:p-0">
      <div class="lg:self-start">
        <h1 class="text-lg">
          Contact Me
        </h1>
        <h3 class="text-6xl">
          Get In Touch
        </h3>
      </div>
      <div class="grid lg:grid-cols-4 gap-8">
        <div class="p-8 shadow-lg col-span-3">
          <contact-me-form />
        </div>
        <div class="lg:flex flex-row hidden lg:grid lg:grid-rows-4 gap-8 lg:col-span-1">
          <contact-card />
          <contact-card />
          <contact-card />
          <contact-card />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ContactMeForm from '~/components/ContactMeForm';
import ContactCard from '~/components/ContactCard';
export default {
  components: ContactMeForm, ContactCard
};
</script>
