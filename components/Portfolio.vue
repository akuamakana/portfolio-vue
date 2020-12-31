<template>
  <div class="flex w-screen justify-center my-8">
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
        <PortfolioCard />
        <PortfolioCard />
        <PortfolioCard />
        <PortfolioCard />
      </div>
    </div>
  </div>
</template>

<script>
import PortfolioCard from '~/components/PortfolioCard';
export default {
  components: PortfolioCard
};
</script>
