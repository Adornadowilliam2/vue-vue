<template>
  <nav class="bg-blue-500 p-2 flex items-center gap-4">
    <img src="./assets/logo.png" class="w-20">
    <h2 class="text-white">{{ title }}</h2>
  </nav>
  <main>
    <div class="card-container flex flex-wrap gap-4 justify-evenly p-4">
      <!-- Use gallery.image to display each image -->
      <div v-for="(gallery) in galleries" :key="gallery.id" class="card border border-black">
        <img :src="gallery.image" class="w-full" alt="Gallery Image">
        <h2>{{ gallery.name }}</h2>
        <!-- Log each gallery object in the console for debugging -->
        {{ console.log(gallery) }}
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      title: "Monk Gallery Photos",
      galleries: [  // Changed from 'index' to 'galleries'
        {
          id: 1,
          name: "Monk Shield the police",
          image: "./assets/image1.png",
        },
        {
          id: 2,
          name: "Monk firing smoke grenade",
          image: "./assets/image2.png",
        },
        {
          id: 3,
          name: "Monk attack the police",
          image: "./assets/image3.png",
        },
        {
          id: 4,
          name: "Image of monk and police",
          image: "./assets/image4.png",
        },
        {
          id: 5,
          name: "The holy kick of monk",
          image: "./assets/image5.png",
        }
      ]
    }
  }
}
</script>

<style>
* {
  padding: 0;
  margin: 0;
}


</style>
