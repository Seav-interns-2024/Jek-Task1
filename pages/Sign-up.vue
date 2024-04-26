<template>
  <v-container fluid class="min-h-screen bg-image">
    <v-row justify="center" align="center" class="h-100">
      <v-col cols="12" sm="8" md="6">
        <v-card class="mt-6 overlay-form">
          <v-card-title class="text-center text-black"> 
            <h2 class="text-3xl font-extrabold">Sign up for an account</h2>
          </v-card-title>
          <v-card-text class="text-black"> 
            <v-form @submit.prevent="signup">
              <v-text-field v-model="form.fullName" label="Full Name" required outlined></v-text-field> 
              <v-text-field v-model="form.email" label="Email address" type="email" required outlined></v-text-field>
              <v-text-field v-model="form.username" label="Username" required outlined></v-text-field>
              <v-text-field v-model="form.password" label="Password" type="password" required outlined></v-text-field>
              <v-checkbox v-model="form.termsAgreed" label="I agree to the terms and conditions"></v-checkbox>
              <v-btn type="submit" color="primary" block>Sign up</v-btn>
            </v-form>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
  setup() {
    const form = ref({
      fullName: '',
      email: '',
      username: '',
      password: '',
      termsAgreed: false
    });

    const signup = () => {
      if (!form.value.termsAgreed) {
        return alert('Please agree to the terms and conditions.');
      }
      console.log('Signing up:', form.value);
    };

    return {
      form,
      signup
    };
  }
});
</script>

<style scoped>
.bg-image {
  background-image: url("assets/css/image/393103237_344118774902943_5589251004004345733_n.png");
  background-size: cover;
}

.overlay-form {
  background-color: rgba(245, 245, 245, 0.781);
  border-radius: 10px;
  padding: 20px;
  box-shadow: 0px 0px 20px rgb(2, 2, 2);
}
</style>
