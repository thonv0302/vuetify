<template>
  <v-app>
    <v-card width="400" class="mx-auto mt-5">
      <v-card-title>Login</v-card-title>
      <v-card-text>
        <v-form>
          <v-text-field
            label="Username"
            prepend-icon="mdi-account-circle"
          ></v-text-field>
          <v-text-field
            :type="showPassword ? 'text' : 'password'"
            label="Password"
            prepend-icon="mdi-lock"
            @click:append-inner-icon="showPassword = !showPassword"
            append-inner-icon="mdi-eye-off"
          ></v-text-field>
        </v-form>
        <v-icon icon="home" />
      </v-card-text>
      <v-card-actions>
        <v-btn color="success">Register</v-btn>
        <v-btn color="info">Login</v-btn>
      </v-card-actions>
    </v-card>
    <!-- <v-main>
      <HelloWorld />
    </v-main> -->
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",

  components: {
    HelloWorld,
  },

  data: () => ({
    //
    showPassword: false,
  }),
};
</script>
