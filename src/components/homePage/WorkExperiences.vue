<script setup lang="ts">
import ExperienceBlock from '../shared/ExperienceBlock.vue';

export type Experience = {
  orgName: string;
  orgLink: string;
  role: string;
  duration: string;
  description?: string;
  technologies?: string[];
};

const experiences: Experience[] = [
  {
    orgName: 'Pathzero',
    orgLink: 'www.pathzero.com',
    role: 'Software Engineer',
    duration: 'DEC 2021 - JUL 2023',
    description:
      "Key player in the rebuild of Pathzero's core SaaS product with a design system, resulting in enhanced user experiences and consistent product design with clean, scalable and maintainable code. Assumed additional responsibilities in Product Management and Design during staff shortages, successfully gathering customer requirements and providing Figma designs and front-end engineering specifications.",
    technologies: ['Vue 3', 'Pinia', 'AWS infrastructure', 'Typescript'],
  },
  {
    orgName: 'Checkbox.ai',
    orgLink: 'www.checkbox.ai',
    role: 'Customer Success Manager',
    duration: 'JUN 2018 - DEC 2021',
    description:
      'Led organisation-wide digital transformation projects for global and national enterprise, amounting to over $250k in directly managed accounts. Co-ordinated pre-sales, training material and customer success strategies, resulting in upsells of over 100k',
  },
];
</script>

<template>
  <div class="experiences">
    <strong>WORK EXPERIENCE</strong>
    <ExperienceBlock
      v-for="experience in experiences"
      :key="experience.orgName"
      :experience="experience"
    >
      <template #experience__description>
        <p>{{ experience.description }}</p>
      </template>
    </ExperienceBlock>
  </div>
</template>

<style scoped lang="scss">
.experiences {
  padding-top: 5rem;
}
</style>
