<template>
    <section class="sponsors">
        <h2>Sponsors</h2>
        <div class="sponsor" v-for="sponsor in sponsors" :key="sponsor.name">
            <img :src="sponsor.logo" :alt="sponsor.name" />
        </div>
    </section>
</template>

<script>

import { defineProps } from 'vue';

const props = defineProps(
    {
        sponsors: {
            type: Array,
            required: true,
            default: () => []
        },

    });

</script>

<style scoped>
.sponsors {
    display: flex;
    justify-content: center;
    gap: 20px;
    background-color: #f8f9fa;
    padding: 20px;
}

.sponsor img {
    width: 100px;
}
</style>