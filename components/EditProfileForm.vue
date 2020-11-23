<template>
<v-container>
  <h5 slot="header" class="title">Edit Profile</h5>
  <v-card class="elevation-0">
    <v-form @submit.prevent="updateProfile">
      <v-row>
        <v-col cols="5">
          <v-text-field
          outlined
            label="Company"
            placeholder="Company"
          >
          </v-text-field>
        </v-col>
        <v-col cols="3">
          <v-text-field
          outlined
            label="Username"
            placeholder="Username"

          >
          </v-text-field>
        </v-col>
        <v-col cols="4">
          <v-text-field
          outlined
            label="Email address"
            placeholder="mike@email.com"
          >
          </v-text-field>
        </v-col>
      </v-row>

      <v-row>
        <v-col cols="6">
          <v-text-field
          outlined
            label="First Name"
            placeholder="First Name"
          >
          </v-text-field>
        </v-col>
        <v-col cols="6">
          <v-text-field
          outlined
            label="Last Name"
            placeholder="Last Name"
          >
          </v-text-field>
        </v-col>
      </v-row>

      <v-row>
        <v-col cols="12">
          <v-text-field
          outlined
            label="Address"
            placeholder="Home Address"
          >
          </v-text-field>
        </v-col>
      </v-row>

      <v-row>
        <v-col cols="4">
          <v-text-field
            label="City"
            outlined
            placeholder="City"
          >
          </v-text-field>
        </v-col>
        <v-col cols="4">
          <v-text-field
          outlined
            label="Country"
            placeholder="Country"
          >
          </v-text-field>
        </v-col>
        <v-col cols="4">
          <v-text-field
          outlined
            label="Postal Code"
            placeholder="ZIP Code"
          >
          </v-text-field>
        </v-col>
      </v-row>

      <v-row>
        <v-col cols="12">
          <v-textarea label="About Me"
          outlined
          >
           
              
            
          </v-textarea>
        </v-col>
      </v-row>

      <v-btn native-type="submit" type="primary" class="btn-fill">
        Save
      </v-btn>
    </v-form>
  </v-card>
  </v-container>
</template>
<script>
export default {
  data() {
    return {
      // user: {
      //   company: 'Creative Code Inc.',
      //   username: 'michael23',
      //   email: '',
      //   firstName: 'Mike',
      //   lastName: 'Andrew',
      //   address: 'Bld Mihail Kogalniceanu, nr. 8 Bl 1, Sc 1, Ap 09',
      //   city: 'New York',
      //   country: 'USA',
      //   postalCode: '',
      //   aboutMe: `Lamborghini Mercy, Your chick she so thirsty, I'm in that two seat Lambo.`
      // }
    };
  },
  methods: {
    updateProfile() {
      alert('Your data: ' + JSON.stringify(this.user));
    }
  }
};
</script>
<style></style>
