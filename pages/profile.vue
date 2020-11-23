<template>
    <v-container class="pt-12 px-12">
            <v-card class="elevation-0">
                <v-col cols="8" class="d-flex align-center">
                   <UserCard /> 
                </v-col>
            </v-card>
    </v-container>
</template>
<script>
import UserCard from '../components/UserCard.vue';

export default {
    components: {
        UserCard
    }
}
</script>