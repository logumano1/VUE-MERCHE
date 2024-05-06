<!--
  This example requires some changes to your config:
  
  ```
  // tailwind.config.js
  module.exports = {
    // ...
    plugins: [
      // ...
      require('@tailwindcss/aspect-ratio'),
    ],
  }
  ```
-->
<template>
    <div class="bg-white">
      <div class="mx-auto max-w-2xl px-4 py-16 sm:px-6 sm:py-24 lg:max-w-7xl lg:px-8">
        <h2 class="text-2xl font-bold tracking-tight text-gray-900">Los más vendidos</h2>
  
        <div class="mt-6 grid grid-cols-1 gap-x-6 gap-y-10 sm:grid-cols-2 lg:grid-cols-4 xl:gap-x-8">
          <div v-for="product in products" :key="product.id" class="group relative">
            <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-md bg-gray-200 lg:aspect-none group-hover:opacity-75 lg:h-80">
              <img :src="product.imageSrc" :alt="product.imageAlt" class="h-full w-full object-cover object-center lg:h-full lg:w-full" />
            </div>
            <div class="mt-4 flex justify-between">
              <div>
                <h3 class="text-sm text-gray-700">
                  <a :href="product.href">
                    <span aria-hidden="true" class="absolute inset-0" />
                    {{ product.name }}
                  </a>
                </h3>
                <p class="mt-1 text-sm text-gray-500">{{ product.color }}</p>
              </div>
              <p class="text-sm font-medium text-gray-900">{{ product.price }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  const products = [
    {
      id: 1,
      name: 'Manzana',
      href: '#',
      imageSrc: 'https://supernormal.es/cdn/shop/files/manzanagolden.png?v=1686916884&width=1200',
      imageAlt: "Front of men's Basic Tee in black.",
      price: '$2,15/kg',
      color: 'Roja',
    },
    {
      id: 2,
      name: 'Kiwi',
      href: '#',
      imageSrc: 'https://supernormal.es/cdn/shop/products/kiwi.jpg?v=1681746430&width=1200',
      imageAlt: "Front of men's Basic Tee in black.",
      price: '$3,71/kg',
      color: 'Golden',
    },
    {
      id: 3,
      name: 'Mandarinas',
      href: '#',
      imageSrc: 'https://supernormal.es/cdn/shop/products/mandarinas.png?v=1679932933&width=1200',
      imageAlt: "Front of men's Basic Tee in black.",
      price: '$3,79/kg',
      color: 'Ecológico',
    },
    {
      id: 4,
      name: 'Plátanos',
      href: '#',
      imageSrc: 'https://supernormal.es/cdn/shop/files/platanos.png?v=1699447050&width=1200',
      imageAlt: "Front of men's Basic Tee in black.",
      price: '$5,65/kg',
      color: 'Ecológicos',
    },
    {
      id: 5,
      name: 'Frambuesas',
      href: '#',
      imageSrc: 'https://supernormal.es/cdn/shop/files/frambuesas_785c576a-d5b2-4a59-8579-7cb54c2a6452.jpg?v=1692628546&width=1200',
      imageAlt: "Front of men's Basic Tee in black.",
      price: '$4,72/kg',
      color: 'Roja',
    },
    {
      id: 6,
      name: 'Arándanos',
      href: '#',
      imageSrc: 'https://supernormal.es/cdn/shop/files/arandanos.png?v=1686916112&width=1200',
      imageAlt: "Front of men's Basic Tee in black.",
      price: '$6,21/kg',
      color: 'Golden',
    },
    {
      id: 7,
      name: 'Judías verdes',
      href: '#',
      imageSrc: 'https://supernormal.es/cdn/shop/products/judiasverdes.jpg?v=1681745217&width=1200',
      imageAlt: "Front of men's Basic Tee in black.",
      price: '$3,12/kg',
      color: 'Ecológico',
    },
    {
      id: 8,
      name: 'Limones',
      href: '#',
      imageSrc: 'https://supernormal.es/cdn/shop/products/limonescaja.jpg?v=1679935698&width=1200',
      imageAlt: "Front of men's Basic Tee in black.",
      price: '$3.95/kg',
      color: 'Ecológicos',
    },
    // More products...
  ]
  </script>