<template>
  <div class="container w-screen">
    <div>
      <Navbar />
      <Intro />
      <Portfolio />
      <!-- <AboutMe /> -->
      <Resume />
      <ContactMe />
      <div class="h-64" />
    </div>
  </div>
</template>

<script>
import Intro from '~/components/Intro';
import Navbar from '~/components/Navbar';
import AboutMe from '~/components/AboutMe';
import Resume from '~/components/Resume';
import Portfolio from '~/components/Portfolio';
import ContactMe from '~/components/ContactMe';
export default {
  components: Intro, Navbar, AboutMe, Resume, Portfolio, ContactMe
};
</script>

<style>
  .title {
    font-size: 12rem;
  }
</style>
