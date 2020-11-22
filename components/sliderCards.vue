<template>
  <v-slide-group v-model="model" class="mx-auto" show-arrows>
    <v-slide-item v-for="(card, i) in cards" :key="i">
      <CourseCards
        class="mr-4 my-2 ml-1"
        :course-length="card.time"
        :course-title="card.title"
        :image-src="card.src"
        :teacher-name="card.name"
        :total-students="card.totalStudents"
      ></CourseCards>
    </v-slide-item>
  </v-slide-group>
</template>

<script>
import CourseCards from './CourseCards.vue'
export default {
  name: 'SliderCards',

  components: {
    CourseCards,
  },

  data: () => ({
    model: [],

    cards: [
      {
        title: 'How to design &',
        src: 'https://cdn.vuetifyjs.com/images/cards/house.jpg',
        desc: 'How to design & prototype mobile UI/UX Experience using Figma ',
        flex: 3,
        name: 'Aditya',
        time: '2hr 5min',
        totalStudents: 2291,
        value: 30,
      },
      {
        title:
          'How to design & prototype mobile UI/UX Experience using Figmadfgsdfgsdfgsdfgsdfgsdfgsdfgsdfgsdfgsdfgsdf',
        src: 'https://cdn.vuetifyjs.com/images/cards/road.jpg',
        desc: 'How to design & prototype mobile UI/UX Experience using Figma ',
        flex: 3,
        name: 'Aditya',
        time: '2hr 5min',
        totalStudents: 2291,
        value: 30,
      },
      {
        title: 'How to design & prototype mobile UI/UX Experience using Figma',
        src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg',
        desc: 'How to design & prototype mobile UI/UX Experience using Figma ',
        flex: 3,
        name: 'Aditya',
        time: '2hr 5min',
        totalStudents: 2291,
        value: 30,
      },
      {
        title: 'How to design & prototype mobile UI/UX Experience using Figma ',
        src: 'https://cdn.vuetifyjs.com/images/cards/girl.jpg',
        desc: 'How to design & prototype mobile UI/UX Experience using Figma ',
        flex: 3,
        name: 'Aditya',
        time: '2hr 5min',
        totalStudents: 2291,
        value: 30,
      },
      {
        title: 'How to design & prototype mobile UI/UX Experience using Figma ',
        src: 'https://cdn.vuetifyjs.com/images/cards/girl.jpg',
        desc: 'How to design & prototype mobile UI/UX Experience using Figma ',
        flex: 3,
        name: 'Aditya',
        time: '2hr 5min',
        totalStudents: 2291,
        value: 30,
      },
      {
        title: 'How to design & prototype mobile UI/UX Experience using Figma ',
        src: 'https://cdn.vuetifyjs.com/images/cards/girl.jpg',
        desc: 'How to design & prototype mobile UI/UX Experience using Figma ',
        flex: 3,
        name: 'Aditya',
        time: '2hr 5min',
        totalStudents: 2291,
        value: 30,
      },
    ],
  }),
}
</script>

<style></style>
