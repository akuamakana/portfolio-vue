<template>
  <div class="flex w-screen justify-center my-8">
    <div class="w-3/4">
      <div>
        <h1 class="text-lg">
          My Portfolio
        </h1>
        <h3 class="text-6xl">
          My Recent Work
        </h3>
      </div>
      <div class="grid grid-cols-2 grid-rows-2 gap-8 my-8">
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
