<template>
  <header class="bg-black py-7 shadow-md">
    <div class="container mx-auto flex justify-between items-center">
      <NuxtLink to="/">
        <img src="assets/css/image/427786390_369378882622069_5839003968903186033_n.png" class="h-12 w-auto logo"/>
      </NuxtLink>
      <nav>
        <ul class="flex gap-10">
          <li>
            <NuxtLink
              to="/"
              class="text-white hover:text-red-400 transition-colors duration-300 ease-in-out animate-bounce"
            >Home</NuxtLink>
          </li>
          <li>
            <NuxtLink
              to="/Log-in"
              class="text-white hover:text-red-400 transition-colors duration-300 ease-in-out animate-bounce"
            >Log-in</NuxtLink>
          </li>
          <li>
            <NuxtLink
              to="/Sign-up"
              class="btn bg-white text-black px-4 py-2 rounded-full shadow-md hover:bg-red-600 hover:text-white transition-all duration-300 ease-in-out transform hover:scale-105"
            >Sign-up</NuxtLink>
          </li>
        </ul>
      </nav>
    </div>
  </header>
  <slot />
</template>

<style>
.btn {
  transition: all 0.3s ease-in-out;
}

.btn:hover {
  background-color: #f70000; 
  color: #161414;
  transform: scale(1.05);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

header {
  transition: background-color 0.3s ease-in-out;
}

.logo:hover {
  animation: bounce 0.5s ease-in-out;
}

@keyframes bounce {
  0% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-5px);
  }
  100% {
    transform: translateY(0);
  }
}

.animate-bounce {
  animation: bounce 0.5s ease-in-out;
}

@keyframes bounce {
  0% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-3px);
  }
  100% {
    transform: translateY(0);
  }
}
</style>