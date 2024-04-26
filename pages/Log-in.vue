<template>
  <v-app>
    <v-main>
      <div class="login-container">
        <div class="login-form">
          <v-container class="max-w-md">
            <v-card class="mt-10">
              <v-card-title class="text-center">
                <h2 class="text-3xl font-extrabold text-Black">
                  Account Login
                </h2>
              </v-card-title>
              <v-card-text>
                <v-form @submit.prevent="onSubmit">
                  <v-text-field
                    v-model="email"
                    label="Email address"
                    outlined
                    color="black"
                    placeholder="Email address"
                    required
                  ></v-text-field>
                  <v-text-field
                    v-model="password"
                    label="Password"
                    outlined
                    color="black"
                    placeholder="Password"
                    required
                    type="password"
                  ></v-text-field>
                  <v-checkbox
                    label="Remember me"
                    color="black"
                    class="text-black"
                  ></v-checkbox>
                  <v-btn
                    type="submit"
                    color="primary"
                    dark
                    class="mt-4"
                  >
                    Sign in
                  </v-btn>
                </v-form>
                <v-btn
                  class="ml-auto mt-6 mr-2 " 
                  color="black"
                  @click="forgotPassword"
                >
                  Forgot your password?
                </v-btn>
              </v-card-text>
            </v-card>
          </v-container>
        </div>
        <div class="image-container">
          <img src="assets/css/image/434056291_954604632986262_8628390014500318754_n.png" alt="Background Image" class="background-image">
        </div>
      </div>
    </v-main>
  </v-app>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const email = ref('');
const password = ref('');   

const onSubmit = () => {
  console.log('Login', { email: email.value, password: password.value});
};

const forgotPassword = () => {
};
</script>

<style>
.login-container {
  display: flex;
  background-color: #ccc; 
  height: 100vh;
}

.login-form {
  flex: 1;
}

.image-container {
  flex: 1;
  display: flex;
  justify-content: flex-end;
}

.background-image {
  max-width: 100%;
  max-height: 100%;
}
</style>