<script>
import { list } from 'postcss';

  export default {
   data() {
     return {
       msg: 'Hello Vue 3 + Vite + Tailwind CSS',
       status: true,
       count: 0,
       list: ['a', 'b', 'c']
     }
   },
  };
</script>

<template>
  <div class="min-h-screen flex flex-col items-center justify-center bg-gray-100">
    <h1 class="text-4xl font-bold mb-4">{{ msg }}</h1>
    <button 
      @click="status = !status" 
      class="px-4 py-2 bg-blue-500 text-white rounded hover:bg-blue-600 transition"
    >
      Toggle Status
    </button>
    <p class="mt-4 text-xl" :class="status ? 'text-green-500' : 'text-red-500'">
      Status is: {{ status ? 'Active' : 'Inactive' }}
    </p>
    <div>
      <button 
        @click="count++" 
        class="mt-6 px-4 py-2 bg-green-500 text-white rounded hover:bg-green-600 transition"
      >
        Increment Count
      </button>
      <button 
        @click="count--" 
        class="mt-6 ml-4 px-4 py-2 bg-red-500 text-white rounded hover:bg-red-600 transition"
      >
        Decrement Count
      </button>

      <button 
        @click="count = 0" 
        class="mt-6 ml-4 px-4 py-2 bg-gray-500 text-white rounded hover:bg-gray-600 transition"
      >
        Reset Count
      </button>

      <p class="text-center mt-4" >{{ count }}</p>
    </div>
  </div>
  <!-- <div>
    <ul class="mt-6 list-disc list-inside">
      <li v-for="(item, index) in list" :key="index" class="text-lg">
        {{ item }}
      </li>
    </ul>
  </div> -->
</template>
