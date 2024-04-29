<template>
  <div class="flex justify-between bg-slate-900 text-white px-20 py-5">
    <div class="flex gap-7">
       
        <a v-for="item in menu" :key="item.name" :href="item.href" class="">{{ item.name }}</a>
    </div>
    <div class="flex gap-7">
        <div class="flex items-center gap-2">
        <a href="#prices"><button>Login</button></a>
        <GlobeAltIcon  class="h-4 w-4"/>
       </div>
       
        <button>Sign up</button>
    </div>
  </div>
</template>

<script setup>


const menu = [
    { name: 'Inicio', href: '#'},
    { name: 'Productos', href: '#'},
    { name: 'Servicios', href: '#prices'},
    { name: 'Contacto', href: '#'},
  ]
  import { GlobeAltIcon } from "@heroicons/vue/24/outline"
  </script>


