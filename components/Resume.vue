<template>
  <div class="w-screen flex justify-center bg-gray-100 py-8">
    <div class="w-1/2">
      <div>
        <h1 class="text-lg">
          My Resume
        </h1>
        <h3 class="text-6xl">
          My Work History
        </h3>
      </div>
      <div class="grid grid-rows-2 grid-cols-2 gap-8 my-8">
        <ResumeCard
          v-for="job in resume"
          :key="job.title"
          :job="job"
        />
        <!-- <ResumeCard />
        <ResumeCard />
        <ResumeCard /> -->
      </div>
    </div>
  </div>
</template>

<script>
import ResumeCard from '~/components/ResumeCard';
export default {
  components: ResumeCard,
  data() {
    return{
      resume: [
        {
          'title': 'Clinical Support Specialist I',
          'dates': 'Jan 2020 - Oct 2020',
          'company': 'Cleveland Clinic',
          'skills': [ 'Managed phones, servers, workstations, etc.', 'Coordinated large scale projects with vendors and clients', 'Provided support for multiple sites and remote users', 'Able to support and coordinate users being moved to remote due to pandemic' ]
        },
        {
          'title': 'Desktop Support Associate',
          'dates': 'May 2017 - Oct 2019',
          'company': 'Kaiser Permanente',
          'skills': [ 'Provided day to day technical support at an enterprise level via ServiceNow.', 'Lead various projects to completion.', 'Utilized various programming languages to implement new and/or better processes for tasks.', 'Played key roles in the completion of multiple IT related projects.', 'Developed extensive understanding of computer systems for efficient analysis and resolution of issues.', 'Managed thousands of assets with great accuracy.' ]
        },        
        {
          'title': 'Intermediate PC Workstation Technician',
          'dates': 'Sept 2015 - Oct 2016',
          'company': 'Kaiser Permanente',
          'skills': [ 'Lead lifecycle refresh project that completed the migration of +5,000 workstations.', 'Gained experience working on medical, pharmaceutical, and call center systems in fast paced environments.', 'Assisted with completion of tickets and projects.', 'Trained incoming technicians.' ]
        },        
        {
          'title': 'Associate PC Workstation Technician ',
          'dates': 'Sept 2014 - July 2015',
          'company': 'Kaiser Permanente',
          'skills': [ 'Deployed thousands of workstations for the refresh project.', 'Completed tasks and tickets via Remedy ticketing system.', 'Created and implemented a new process that led to my team’s early completion of the refresh project.', 'Assisted other teams with completion of the refresh project.' ]
        }
      ]
    };
  }
};
</script>
