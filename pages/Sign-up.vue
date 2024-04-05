<template>
    <div class="min-h-screen flex justify-center bg-gray-800 relative">
      <div class="max-w-md w-full space-y-8 z-10">
        <div>
          <h2 class="mt-6 text-center text-3xl font-extrabold text-black  px-4 py-2 rounded-full shadow-md bg-black text-white">
            Sign up for an account
          </h2>
        </div>
        <form class="mt-8 space-y-6" @submit.prevent="signup">
          <div class="rounded-md shadow-sm -space-y-px">
            <div>
              <label for="full-name" class="sr-only">Full Name</label>
              <input id="full-name" name="full-name" type="text" autocomplete="name" required v-model="fullName" class="appearance-none rounded-none relative block w-full px-3 py-2 border border-gray-300 placeholder-gray-500 text-gray-900 rounded-t-md focus:outline-none focus:ring-green-500 focus:border-green-500 focus:z-10 sm:text-sm" placeholder="Full Name">
            </div>
            <div>
              <label for="email-address" class="sr-only">Email address</label>
              <input id="email-address" name="email" type="email" autocomplete="email" required v-model="email" class="appearance-none rounded-none relative block w-full px-3 py-2 border border-gray-300 placeholder-gray-500 text-gray-900 focus:outline-none focus:ring-green-500 focus:border-green-500 focus:z-10 sm:text-sm" placeholder="Email address">
            </div>
            <div>
              <label for="username" class="sr-only">Username</label>
              <input id="username" name="username" type="text" autocomplete="username" required v-model="username" class="appearance-none rounded-none relative block w-full px-3 py-2 border border-gray-300 placeholder-gray-500 text-gray-900 focus:outline-none focus:ring-green-500 focus:border-green-500 focus:z-10 sm:text-sm" placeholder="Username">
            </div>
            <div>
              <label for="password" class="sr-only">Password</label>
              <input id="password" name="password" type="password" autocomplete="new-password" required v-model="password" class="appearance-none rounded-none relative block w-full px-3 py-2 border border-gray-300 placeholder-gray-500 text-gray-900 rounded-b-md focus:outline-none focus:ring-green-500 focus:border-green-500 focus:z-10 sm:text-sm" placeholder="Password">
            </div>
          </div>
  
          <div class="flex items-center justify-between">
            <div>
              <input id="terms" name="terms" type="checkbox" class="h-4 w-4 text-gray-600 focus:ring-gray-500 border-gray-300 rounded">
              <label for="terms" class="ml-2 block text-sm text-white">
                I agree to the <a href="#" class="underline">terms and conditions</a>
              </label>
            </div>
          </div>
  
          <div>
            <button type="submit" class="group relative w-full flex justify-center py-2 px-4 border border-transparent text-sm font-medium rounded-md text-white bg-black hover:bg-red-800 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-green-500">
              <span class="absolute left-0 inset-y-0 flex items-center pl-3">
              </span>
              Sign up
            </button>
          </div>
        </form>
      </div>
  
      <div class="absolute inset-0 md:hidden">
        <img src="assets/css/image/393103237_344118774902943_5589251004004345733_n.png" alt="Your Image" class="object-cover h-full w-full">
      </div>
      <div class="hidden md:block absolute inset-0">
        <img src="assets/css/image/393103237_344118774902943_5589251004004345733_n.png" alt="Your Image" class="object-cover h-full w-full">
      </div>
    </div>
  </template>
  
  <script setup>
    import { ref } from 'vue';
  
    const fullName = ref('');
    const email = ref('');
    const username = ref('');
    const password = ref('');
  
    const signup = () => {
      console.log('Signing up:', { fullName: fullName.value, email: email.value, username: username.value, password: password.value });
    };
  </script>