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
    <div class="bg-white" id="verdura">
      <div class="mx-auto max-w-2xl px-4 py-16 sm:px-6 sm:py-24 lg:max-w-7xl lg:px-8">
        <h2 class="text-2xl font-bold tracking-tight text-gray-900">Verduras</h2>
  
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
      name: 'Esparrago blanco',
      href: '#',
      imageSrc: 'https://supernormal.es/cdn/shop/files/Esparragosblancos.jpg?v=1712591134&width=1200',
      imageAlt: "Front of men's Basic Tee in black.",
      price: '$2,15/kg',
      color: 'Ecológico',
    },
    {
      id: 2,
      name: 'Brócoli',
      href: '#',
      imageSrc: 'https://supernormal.es/cdn/shop/products/brocoli.png?v=1679933437&width=1200',
      imageAlt: "Front of men's Basic Tee in black.",
      price: '$3,71/kg',
      color: 'Ecológico',
    },
    {
      id: 3,
      name: 'Puerros',
      href: '#',
      imageSrc: 'https://supernormal.es/cdn/shop/products/puerros_6e85f6d1-b59f-4b7d-973c-384f8a5cf84f.jpg?v=1681745547&width=1200',
      imageAlt: "Front of men's Basic Tee in black.",
      price: '$3,79/kg',
      color: 'Ecológico',
    },
    {
      id: 4,
      name: 'Acelga',
      href: '#',
      imageSrc: 'https://supernormal.es/cdn/shop/products/acelgaverde.png?v=1679933289&width=1200',
      imageAlt: "Front of men's Basic Tee in black.",
      price: '$5,65/kg',
      color: 'Ecológicos',
    },
    {
      id: 5,
      name: 'Cebollas',
      href: '#',
      imageSrc: 'https://supernormal.es/cdn/shop/products/cebollas1.jpg?v=1679933519&width=1200',
      imageAlt: "Front of men's Basic Tee in black.",
      price: '$4,72/kg',
      color: 'Ecológico',
    },
    {
      id: 6,
      name: 'Patatas ',
      href: '#',
      imageSrc: 'https://supernormal.es/cdn/shop/products/patatastipo1_879fccfc-9b0a-43f9-97a8-7363d0974069.jpg?v=1679934838&width=1200',
      imageAlt: "Front of men's Basic Tee in black.",
      price: '$6,21/kg',
      color: 'Ecológico',
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
      name: 'Alcachofas',
      href: '#',
      imageSrc: 'https://supernormal.es/cdn/shop/products/alcachofas.png?v=1680116651&width=1200',
      imageAlt: "Front of men's Basic Tee in black.",
      price: '$3.95/kg',
      color: 'Ecológicos',
    },
    // More products...
  ]
  </script>