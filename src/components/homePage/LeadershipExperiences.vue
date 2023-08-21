<script setup lang="ts">
import ExperienceBlock from '../shared/ExperienceBlock.vue';
import type { Experience } from './WorkExperiences.vue';

const experiences: Experience[] = [
  {
    orgName: '180 Degrees Consulting',
    orgLink: 'www.180dc.org',
    role: 'Vice President of Consulting',
    duration: 'JUL 2018 - DEC 2021',
  },
];
</script>

<template>
  <div class="experiences">
    <strong>LEADERSHIP EXPERIENCE</strong>
    <ExperienceBlock
      v-for="experience in experiences"
      :key="experience.orgName"
      :experience="experience"
    >
      <template #experience__description>
        <ul>
          <li>
            As VP of Consulting: Organised 20+ consulting projects for over 120 students with
            mentoring from McKinsey, BCG and Bain mentors.
          </li>
          <li>
            As Consulting Director: Improved internal processes and training to improve the quality
            of consulting experience for students and clients.
          </li>
          <li>
            As Project Leader: Recommended a website redesign from heuristic-led principles to
            increase volunteer acquisition by 120%.
          </li>
        </ul>
      </template>
    </ExperienceBlock>
  </div>
</template>

<style scoped lang="scss">
.experiences {
  padding-top: 2rem;
}
</style>
