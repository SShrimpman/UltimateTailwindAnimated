<template>
  <div class="flex flex-col justify-center items-center h-screen">
    <h1 class="mb-4 text-4xl font-extrabold leading-none tracking-tight text-gray-900 md:text-5xl lg:text-6xl dark:text-white">
      Ultimate TailwindCSS Tutorial
    </h1>
    <p class="mb-6 text-lg font-normal text-gray-500 lg:text-xl sm:px-16 xl:px-48 dark:text-gray-400">
      See my cool cat in the next page
    </p>
    <router-link to="/secondpage">
      <a href="/#" class="inline-flex items-center justify-center px-5 py-3 text-base font-medium text-center text-green-500 bg-gray-900 rounded-3xl hover:text-white hover:bg-green-600 hover:rounded-xl transition-all duration-300 ease-linear">
        See cat
        
      </a>
    </router-link>
  </div>

</template>