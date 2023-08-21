<script setup lang="ts">
import type { Experience } from '../homePage/WorkExperiences.vue';

interface Props {
  experience: Experience;
}
const props = defineProps<Props>();
</script>

<template>
  <div class="experience">
    <div class="duration">
      {{ props.experience.duration }}
    </div>
    <div class="details">
      <a :href="props.experience.orgLink" target="_blank">{{ props.experience.orgName }}</a>
      <div>{{ props.experience.role }}</div>
      <slot class="description" name="experience__description"></slot>
      {{ props.experience.technologies }}
    </div>
  </div>
</template>

<style scoped lang="scss">
.experience {
  padding: 1rem 2rem 3rem;
  color: var(--dull-white);
  display: flex; // TODO: remove flex for smaller widths

  .duration {
    padding-right: 2rem;
    min-width: 10rem;
  }
  .details {
    max-width: 40rem;
  }
}
</style>
