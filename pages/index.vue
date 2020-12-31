<template>
  <div class="container w-screen">
    <navbar />
    <intro />
    <portfolio />
    <!-- <AboutMe /> -->
    <resume />
    <contact-me />
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
