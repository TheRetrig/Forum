<template>
  <v-row>
    <v-col cols="8"><edit-profile-form> </edit-profile-form></v-col>
    <v-col cols="4"><user-card> </user-card></v-col>
  </v-row>
</template>
<script>
import EditProfileForm from '../components/EditProfileForm.vue';
import UserCard from '../components/UserCard.vue';

export default {
  name: 'user',
  components: {
    EditProfileForm,
    UserCard
  }
};
</script>
<style></style>