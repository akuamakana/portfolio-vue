<template>
  <div class="w-screen flex justify-center bg-gray-100 py-8">
    <div class="w-1/2">
      <div>
        <h1 class="text-lg">My Resume</h1>
        <h3 class=text-6xl>My Work History</h3>
      </div>
      <div class='grid grid-rows-2 grid-cols-2 gap-8 my-8'>
        <ResumeCard />
        <ResumeCard />
        <ResumeCard />
        <ResumeCard />
      </div>
    </div>
  </div>
</template>

<script>
import ResumeCard from '~/components/ResumeCard'
export default {
  
}
</script>