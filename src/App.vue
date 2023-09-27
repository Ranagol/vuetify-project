<template>
  <v-app>
    <!-- App bar -->
    <v-app-bar app color="primary" dark>
      <v-toolbar-title>Vuetify dashboard</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn to="/" rounded>Home</v-btn>
      <v-btn to="/login" rounded>Login</v-btn>
    </v-app-bar>

    <!-- ROUTER -->
    <br>
    <br>
    <br>
    <br>

    <v-content>
      <router-view></router-view>
    </v-content>


    <!-- Footer -->
    <div>
      <br>
      <v-footer class="bg-grey-lighten-1">
        <v-row justify="center" no-gutters>
          <v-btn
            v-for="link in links"
            :key="link"
            color="white"
            variant="text"
            class="mx-2"
            rounded="xl"
          >
            {{ link }}
          </v-btn>
          <v-col class="text-center mt-1" cols="12">
            {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
          </v-col>
        </v-row>
      </v-footer>
    </div>



  </v-app>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Login from '@/views/Login.vue';

export default defineComponent({
  name: 'App',
  components: {},
  data() {
    return {
      showPassword: false,
      links: [
        'Home',
        'About Us',
        'Team',
        'Services',
        'Blog',
        'Contact Us',
      ],
    }
  },
});

</script>
