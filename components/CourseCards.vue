<template>
  <v-card width="280px" height="360" class="d-flex flex-column">
    <v-img :src="imageSrc" height="160px"> </v-img>
    <v-row align="center" justify="space-between" no-gutters>
      <v-col>
        <v-card-text
          class="text-caption black--text"
          v-text="totalStudents + ' Students'"
        ></v-card-text>
      </v-col>

      <v-col>
        <v-card-text
          class="text-caption text-right black--text"
          v-text="courseLength"
        ></v-card-text>
      </v-col>
    </v-row>

    <div style="height: 96px">
      <v-card-title class="black--text font-weight-medium py-0">
        <v-clamp autoresize :max-lines="3">{{ courseTitle }} </v-clamp>
      </v-card-title>
    </div>
    <v-spacer></v-spacer>
    <v-card-actions class="pa-0">
      <v-card-text v-text="'By ' + teacherName"></v-card-text>
      <v-spacer></v-spacer>
      <v-btn icon>
        <v-spacer />
        <v-icon> mdi-bookmark-outline </v-icon>
      </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
import VClamp from 'vue-clamp'
export default {
  name: 'CourseCard',
  components: {
    VClamp,
  },
  props: {
    imageSrc: {
      type: String,
      default: 'Loading...',
    },
    teacherName: {
      type: String,
      default: 'Loading...',
    },
    courseLength: {
      type: String,
      default: 'Loading...',
    },
    courseTitle: {
      type: String,
      default: 'Loading...',
    },
    totalStudents: {
      type: Number,
      default: 0,
    },
  },
}
</script>

<style></style>
