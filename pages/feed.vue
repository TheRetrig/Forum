<template>
  <div>
    <v-img
      height="519px"
      class="d-flex align-center"
      src="https://images.unsplash.com/photo-1517512006864-7edc3b933137?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80"
      gradient="to top right,  rgba(121, 121, 121, 0.33), rgba(51, 51, 51, 0.7)"
    >
      <v-container>
        <div class="container white--text text-h5">By Alethiea</div>
        <div class="container white--text text-h2 font-weight-bold">
          Galore : Decentralised Forum Platform
        </div>

        <div class="container white--text text-h5 font-weight-bold">
          Join Us In revolutionizing your web experience
        </div>

        <!-- <v-container>
            <v-btn large class="btn-text text-h6 text-capitalize" color="white"
              >Join</v-btn
            >
          </v-container> -->
      </v-container>
    </v-img>
    <!-- pass props in Post  -->
    <v-container v-for="(card, i) in cards" :key="i">
      <Feed />
    </v-container>
    <!-- pass props in Post  -->
  </div>
</template>

<script>
import Feed from "../components/Feed";
export default {
  components: {
    Feed,
  },
  data: () => ({
    cards: {},
  }),
};
</script>