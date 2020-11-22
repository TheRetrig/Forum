<template>
  <div>
    <v-card class="mx-auto" max-width="500">
      <div class="container d-flex px-4">
        <v-avatar color="brown">
          <span class="white--text headline">AR</span>
        </v-avatar>
        <div class="d-flex flex-column pl-4">
          <h4>{{ fullName }}</h4>
          <h6 class="caption">
            {{ email }}
          </h6>
          <p class="caption">
            {{ time }}
          </p>
        </div>
      </div>

      <v-card-title> {{ title }} </v-card-title>
        <v-card-subtitle>
            <v-clamp autoresize :max-lines="2">{{ textDesc }}</v-clamp>
        </v-card-subtitle>
      <v-card-subtitle>
        
      </v-card-subtitle>
      <v-img
        src= {{ imgUrl }}
        height="200px"
      ></v-img>
      <div class="container d-flex">
        <p>{{ likes }} Likes</p>
        <v-spacer></v-spacer>
        <p>{{ comments }} Comments</p>
      </div>
      <v-divider></v-divider>
      <div class="container d-flex">
        <v-btn class="elevation-0" @click="changeLike">
          <div>
            <v-icon>mdi-thumb-up-outline</v-icon> Like
          </div>
        </v-btn>
        <v-spacer></v-spacer>
        <v-btn class="elevation-0" @click="show = !show"
          ><v-icon>mdi-comment-outline</v-icon> Comment</v-btn
        >
        <v-spacer></v-spacer>
        <p><v-icon>mdi-share-variant</v-icon> Share</p>
      </div>
      <v-divider></v-divider>

      <v-expand-transition>
        <div v-show="show">
          <div class="d-flex container">
            <v-avatar color="brown">
              <span class="white--text headline">AR</span>
            </v-avatar>
            <v-textarea
              filled
              label="Mike"
              readonly
              value="The Woodman set to work at once, and so sharp was his axe that the tree was soon chopped nearly through."
            ></v-textarea>
          </div>
        </div>
      </v-expand-transition>
    </v-card>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      likeIcon: 'mdi-thumb-up-outline',
  methods: {
    changeLike() {
      this.likeIcon = 'mdi-thumb-up'
    },
  },
  props: {
    initials: String,
    fullName: String,
    email: String,
    time: String,    
    title: String,
    textDesc: String,
    imgUrl: String,
    likes: Number,
    comments: Number,
    isLiked: Boolean,
    commentIds: Array,
    author: Object,
    callback: Function,
    contactsPromise: Promise 
},
}
  }
}
</script>


