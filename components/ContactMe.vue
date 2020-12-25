<template>
  <div class="flex flex-col w-screen justify-center items-center py-8">
    <div class="w-1/2">
      <div class="self-start">
        <h1 class="text-lg">
          Contact Me
        </h1>
        <h3 class="text-6xl">
          Get In Touch
        </h3>
      </div>
      <div class="grid grid-cols-4 gap-8">
        <div class="p-8 shadow-lg col-span-3">
          <ContactMeForm />
        </div>
        <div class="grid grid-rows-4 gap-8 col-span-1">
          <ContactCard />
          <ContactCard />
          <ContactCard />
          <ContactCard />
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
