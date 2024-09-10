<template>
    <BannerSection />
  <HeaderSection />

  <SpeakerSection />
  <ProgramSection :program="program1" day ="Day 1 : September 17, 2024" />
  <ProgramSection :program="program2" day ="Day 2 : September 18, 2024"/>

  <SponsorsSection :sponsors="sponsors" />
  <OrganizerSection :organizers="organizers" />
  <FooterSection />

</template>

<script setup>
import HeaderSection from '../components/HeaderSection.vue';
import FooterSection from '../components/FooterSection.vue';
import SpeakerSection from '../components/SpeakerSection.vue';
import ProgramSection from '../components/ProgramSection.vue';
import SponsorsSection from '../components/SponsorsSection.vue';
import OrganizerSection from '../components/OrganizerSection.vue';
import BannerSection from '../components/BannerSection.vue';





const program1 = [
  {
    id: 1,
    date: 'September 17, 2024',
    time: '8:30 AM - 9:00 AM',
    title: 'Participant Reception',
    speaker: null,
    affiliation: 'University of Yaoundé 1'
  },
  {
    id: 2,
    date: 'September 17, 2024',
    time: '9:00 AM - 9:30 AM',
    title: 'Opening Speech + Group Photo',
    speaker: null,
    affiliation: 'University of Yaoundé 1'
  },
  {
    id: 3,
    date: 'September 17, 2024',
    time: '9:30 AM - 10:00 AM',
    title: 'Coffee Break',
    speaker: null,
    affiliation: 'University of Yaoundé 1'
  },
  {
    id: 4,
    date: 'September 17, 2024',
    time: '10:00 AM - 11:45 AM',
    title: 'Presentation 1: Data in AI',
    speaker: 'Dr. Hyppolyte Tapamo',
    affiliation: 'University of Yaoundé 1'
  },
  {
    id: 5,
    date: 'September 17, 2024',
    time: '11:45 AM - 12:30 PM',
    title: 'Presentation 2: Data Collection: Process, Constraints, and Best Practices',
    speaker: 'Prof. Norbert Tsopzé',
    affiliation: 'University of Yaoundé 1'
  },
  {
    id: 6,
    date: 'September 17, 2024',
    time: '12:30 PM - 1:30 PM',
    title: 'Lunch Break',
    speaker: null,
    affiliation: 'University of Yaoundé 1'
  },
  {
    id: 7,
    date: 'September 17, 2024',
    time: '1:30 PM - 2:15 PM',
    title: 'Presentation 3: Material Production Processes: Data Generation',
    speaker: 'Prof. Elie Kamseu / Franck Menkam',
    affiliation: 'University of Yaoundé 1'
  },
  {
    id: 8,
    date: 'September 17, 2024',
    time: '2:15 PM - 3:00 PM',
    title: 'Workshop 1: Data in Materials Science (Nature and Use)',
    speaker: 'Herman Tcheneghon',
    affiliation: 'University of Yaoundé 1'
  },
  {
    id: 9,
    date: 'September 17, 2024',
    time: '3:00 PM - 3:45 PM',
    title: 'Workshop 2: Data Collection: Scraping',
    speaker: 'Claude Tinku',
    affiliation: 'University of Yaoundé 1'
  },
  {
    id: 10,
    date: 'September 17, 2024',
    time: '3:45 PM - 4:30 PM',
    title: 'Workshop 3: Data Augmentation (Text, Images, Audio)',
    speaker: 'Herman Tcheneghon',
    affiliation: 'University of Yaoundé 1'
  }
];

const program2 = [
{
    id: 11,
    date: 'September 18, 2024',
    time: '8:30 AM - 10:00 AM',
    title: 'Inaugural Lecture: Leveraging Artificial Intelligence (AI) and Generative AI for Enhanced Materials Science: Concepts, Empirical Insights and Future Directions',
    speaker: 'Prof. Samuel Fosso Wamba',
    affiliation: 'University of Yaoundé 1'
  },
  {
    id: 12,
    date: 'September 18, 2024',
    time: '10:00 AM - 10:45 AM',
    title: 'Presentation 4: Data Sharing: Licenses, Open Data, and Ethics',
    speaker: 'Dr. Hyppolyte Tapamo',
    affiliation: 'University of Yaoundé 1'
  },
  {
    id: 13,
    date: 'September 18, 2024',
    time: '10:45 AM - 11:30 AM',
    title: 'Presentation 5: Scientific Publication: Data Papers',
    speaker: 'Dr. Thomas Messie',
    affiliation: 'University of Yaoundé 1'
  },
  {
    id: 14,
    date: 'September 18, 2024',
    time: '11:30 AM - 12:00 PM',
    title: 'Coffee Break',
    speaker: null,
    affiliation: 'University of Yaoundé 1'
  },
  {
    id: 15,
    date: 'September 18, 2024',
    time: '12:00 PM - 12:45 PM',
    title: 'Presentation 6: The EPPER Project: Execution and Results',
    speaker: 'Dr. Tiogning',
    affiliation: 'University of Yaoundé 1'
  },
  {
    id: 16,
    date: 'September 18, 2024',
    time: '12:45 PM - 1:30 PM',
    title: 'Workshop 4: Data Preprocessing (Cleaning, Imbalance, Segmentation, ...)',
    speaker: 'Stella Ananjou',
    affiliation: 'University of Yaoundé 1'
  },
  {
    id: 17,
    date: 'September 18, 2024',
    time: '1:30 PM - 2:45 PM',
    title: 'Workshop 5: Statistical Data Analysis',
    speaker: 'Herman Tcheneghon',
    affiliation: 'University of Yaoundé 1'
  },
  {
    id: 18,
    date: 'September 18, 2024',
    time: '2:45 PM - 3:45 PM',
    title: 'Lunch Break',
    speaker: null,
    affiliation: 'University of Yaoundé 1'
  },
  {
    id: 19,
    date: 'September 18, 2024',
    time: '3:45 PM - 4:30 PM',
    title: 'Workshop 6: Data Visualization',
    speaker: 'Sherelle Kana',
    affiliation: 'University of Yaoundé 1'
  },
  {
    id: 20,
    date: 'September 18, 2024',
    time: '3:30 PM - 4:30 PM',
    title: 'Networking and Closing',
    speaker: null,
    affiliation: 'University of Yaoundé 1'
  }
]




const sponsors = [
  { name: 'Sponsor 1', logo: 'path/to/logo' },
  { name: 'Sponsor 2', logo: 'path/to/logo' }
  // Add more sponsors here
]
const organizers = [
  { name: 'Organizer 1', logo: 'path/to/logo' },
  { name: 'Organizer 2', logo: 'path/to/logo' }
  // Add more organizers here
]
</script>
