<template>
  <div class="rounded-lg shadow-lg grid grid-rows-6">
    <img
      class="row-span-5 rounded-t-lg"
      :src="require(`~/assets/images/${project.image}.png`)"
      alt="project.title"
    >
    <div class="px-4 py-2 flex justify-between items-center">
      <div class="text-2xl">
        {{ project.title }}
      </div>
      <div class="grid grid-cols-2 gap-4">
        <a
          target="_blank"
          :href="project.liveLink"
          class="rounded-lg text-center font-bold bg-green-400 text-white px-6 py-2"
        >Live</a>
        <a
          target="_blank"
          :href="project.gitLink"
          class="rounded-lg text-center font-bold bg-green-400 text-white px-6 py-2"
        >Github</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: [ 'project' ]
};
</script>
