<template>
    <section class="organizers">
      <h2>Organizers</h2>
      <div class="organizer" v-for="organizer in organizers" :key="organizer.name">
        <img :src="organizer.logo" :alt="organizer.name" />
      </div>
    </section>
  </template>

<script>

import { defineProps } from 'vue';

const props = defineProps(
    {
        organizers: {
            type: Array,
            required: true,
            default: () => []
        },

    });

console.log(props);
</script>

<style scoped>

.organizers {
  display: flex;
  justify-content: center;
  gap: 20px;
  padding: 20px;
}
.organizer img {
  width: 100px;
}
</style>