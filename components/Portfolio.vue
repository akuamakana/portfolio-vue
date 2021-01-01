<template>
  <div id="portfolio" class="flex w-screen justify-center my-8 lg:mt-40">
    <div class="lg:w-3/4 flex-auto px-4 lg:flex-none lg:p-0">
      <div>
        <h1 class="text-lg">
          My Portfolio
        </h1>
        <h3 class="text-6xl">
          My Recent Work
        </h3>
      </div>
      <div class="grid lg:grid-cols-2 grid-rows-2 gap-8 my-8">
        <PortfolioCard
          v-for="(project, index) in projects"
          :key="index"
          :project="project"
        />
      </div>
    </div>
  </div>
</template>

<script>
import PortfolioCard from '~/components/PortfolioCard';
export default {
  components: PortfolioCard,
  data() {
    return {
      projects: [ {
        title: 'Portfolio',
        image: 'portfolio',
        gitLink: 'https://github.com/akuamakana/portfolio-vue',
        liveLink: 'https://www.kionkaimi.com'
      },
      {
        title: 'Recipe App',
        image: 'recipes',
        gitLink: 'https://github.com/akuamakana/recipe-app',
        liveLink: 'https://kion-recipes-app.netlify.app/'
      },
      {
        title: 'BMR & Macro Calculator',
        image: 'bmr',
        gitLink: 'https://github.com/akuamakana/bmr-macro-calculator',
        liveLink: 'https://bmr-macro-calculator.netlify.app/'
      },
      {
        title: 'Pin Kaow Thai Restaurant',
        image: 'restaurant',
        gitLink: 'https://github.com/akuamakana/restaurant',
        liveLink: 'https://pinkaow-restaurant.netlify.app/'
      } ]
    };
  }
};
</script>
