<template>
    <!-- Login component -->
    <v-card width="400" class="mx-auto mt-5">
      <v-card-title>
        <h1 class="display-1">Login</h1>
      </v-card-title>
      <v-card-text>
        <v-form>

          <!-- USERNAME -->
          <v-text-field
            label="Username"
            prepend-icon="mdi-account-circle"
          />

          <!-- PASSWORD -->
          <v-text-field
            :type="showPassword ? 'text' : 'password'"
            label="Password"
            prepend-icon="mdi-lock"
            :append-icon="showPassword ? 'md-eye' : 'mdi-eye-off'"
            @click:append="showPassword = !showPassword"
          />
          <!-- @click:append = this means: if the user clicks on the appended icon, then... -->
        </v-form>
      </v-card-text>
      <v-divider></v-divider>
      <v-card-actions>

        <!-- BUTTONS -->
        <v-btn color="success">Register</v-btn>
        <v-spacer></v-spacer>
        <v-btn color="info">Login</v-btn>
      </v-card-actions>
    </v-card>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'LoginPage',
  components: {},
  data() {
    return {
      showPassword: false,
    }
  },
});

</script>
