<template>
    <div>
      <div>
         <img src="assets/css/image/sukuna.gif" class="img-background" /> -->
      </div>
      <main class="container mx-auto py-8 px-4">
        <slot />
      </main>
    </div>
  </template>
  
  <style scoped>
  .btn {
    transition: all 0.3s ease-in-out;
  }
  .img-background {
    @apply h-screen w-screen object-cover;
    opacity: 0.9;
  }
  .btn:hover {
    background-color: bg-red-600;
    color: black;
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
  </style>