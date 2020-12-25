/* eslint-disable vue/require-prop-types */
<template>
  <div class="shadow-md border-l-2 border-orange-400 p-4 bg-white">
    <div class="mb-4">
      <h1 class="font-bold">
        {{ job.title }}
      </h1>
      <span class="text-orange-400">{{ job.dates }}</span><span> | </span><span class="text-gray-700">{{ job.company }}</span>
    </div>
    <ul class="list-disc list-inside break-words">
      <li
        v-for="skill in job.skills"
        :key="skill"
      >
        {{ skill }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: { job: Object }
};
</script>

<style>
  ul {
    columns: 2;
  }
</style>
