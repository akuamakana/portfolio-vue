<template>
  <div class='container w-screen'>
    <div>
      <Navbar />
      <AboutMe />
      <Portfolio />
      <Resume />
      <ContactMe/>
    </div>
  </div>
</template>

<script>
import Navbar from '~/components/Navbar'
import AboutMe from '~/components/AboutMe'
import Resume from '~/components/Resume'
import Portfolio from '~/components/Portfolio'
import ContactMe from '~/components/ContactMe'
export default {
  components: Navbar, AboutMe, Resume, Portfolio, ContactMe
}
</script>

