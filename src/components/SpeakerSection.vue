<template>
    <section class="speakers">
      <h2>Speakers</h2>
      <div class="speaker" v-for="speaker in speakers" :key="speaker.name">
        <img :src="speaker.image" :alt="speaker.name" class="speaker-image" />
        <div class="details">
          <h3>{{ speaker.name }}</h3>
          <p>{{ speaker.role }}</p>
        </div>
      </div> 
    </section>
  </template>

  <script setup>
  import { ref } from 'vue';
  import Wamba from '@/assets/images/wamba.jpeg';
  import Kamseu from "@/assets/images/prof.png"
  import Herman from  "@/assets/images/Tcheneghon.jpeg"
  const speakers = ref([
    {
      name: 'Prof. Samuel Fosso Wamba',
      role: 'Inaugural Lecturer',
      image:Wamba, // Remplacez par le chemin réel
      linkedin: 'https://linkedin.com/in/samuel-fosso-wamba',
      scholar: 'https://scholar.google.com/citations?user=example'
    },
    {
      name: 'Prof. Elie Kamseu',
      role: 'Speaker',
      image: Kamseu, // Remplacez par le chemin réel
      linkedin: 'https://linkedin.com/in/elie-kamseu',
      scholar: 'https://scholar.google.com/citations?user=example'
    },
    {
        name: 'Prof. Norbert Tsopzé',
        role: 'Speaker',
        image: 'path',
        linkedin: 'https://linkedin.com/in/norbert-tsopze',
        scholar: 'https://scholar.google.com/citations?user=example'
    },{
        name: 'Dr. Hyppolyte Tapamo',
        role: 'Speaker',
        image: 'path',
        linkedin: 'https://linkedin.com/in/hyppolyte-tapamo',
        scholar: 'https://scholar.google.com/citations?user=example'
    },{
        name: 'Franck Menkam',
        role: 'Co-Speaker',
        image: 'path',
        linkedin: 'https://linkedin.com/in/franck-menkam',
        scholar: 'https://scholar.google.com/citations?user=example'
    },  {
        name: 'Dr. Tiogning',
        role: 'Speaker',
        image: 'path',
        linkedin: 'https://linkedin.com/in/tiogning',
        scholar: 'https://scholar.google.com/citations?user=example'
    },
    {
        name: 'Dr. Thomas Messi',
        role: 'Speaker',
        image: 'path',
        linkedin: 'https://linkedin.com/in/thomas-messie',
        scholar: 'https://scholar.google.com/citations?user=example'
    },
    {
        name: 'Claude Tinku',
        role: 'Workshop Leader',
        image: 'path',
        linkedin: 'https://linkedin.com/in/claude-tinku',
        scholar: 'https://scholar.google.com/citations?user=example'
    },
    {
        name: 'Herman Tcheneghon',
        role: 'Workshop Leader',
        image: Herman,
        linkedin: 'https://linkedin.com/in/herman-tcheneghon',
        scholar: 'https://scholar.google.com/citations?user=example'
    },
    {
        name: 'Stella Ananjou',
        role: 'Workshop Leader',
        image: 'path',
        linkedin: 'https://linkedin.com/in/stella-ananjou',
        scholar: 'https://scholar.google.com/citations?user=example'
    },
    {
        name: 'Sherelle Kana',
        role: 'Workshop Leader',
        image: 'path',
        linkedin: 'https://linkedin.com/in/sherelle-kana',
        scholar: 'https://scholar.google.com/citations?user=example'
    }
  ]);
  </script>

<style scoped>
.speakers {
  display: flex;
  flex-wrap: wrap;
  gap: 20px; /* Space between columns */
  justify-content: center;
}

.speaker {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 200px; /* Adjust the width as needed */
}

.speaker-image {
  width: 100%;
  height: 200px; /* Adjust the height as needed */
  object-fit: cover;
  border-radius: 50%; /* Makes the image circular */
  border: 2px solid #ddd; /* Optional: adds a border around the image */
}

.details {
  text-align: center;
  margin-top: 10px; /* Space between the image and the text */
}

h3 {
  margin: 0;
  font-size: 1.2em; /* Adjust the font size as needed */
}

p {
  margin: 0;
  color: #555; /* Adjust the color as needed */
}
</style>