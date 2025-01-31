<template>
  <nav class="bg-blue-500 p-2 flex items-center gap-4">
    <img src="./assets/logo.png" class="w-20">
    <h2 class="text-white">{{ title }}</h2>
  </nav>
  <main>
    <div class="card-container flex flex-wrap gap-4 justify-evenly p-4">
      <div v-for="(gallery) in galleries" :key="gallery.id" class="card m-4">
        <img :src="gallery.image" class="w-full" alt="Gallery Image" >
        <h2>{{ gallery.name }}</h2>
   
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
      galleries: [  
        {
          id: 1,
          name: "Monk Shield the police",
          image: "https://github.com/Adornadowilliam2/vue-vue/blob/master/src/assets/image1.png?raw=true",
        },
        {
          id: 2,
          name: "Monk wearing a gas mask",
          image: "https://github.com/Adornadowilliam2/vue-vue/blob/master/src/assets/image2.png?raw=true",
        },
        {
          id: 3,
          name: "Monk vs policies",
          image: "https://github.com/Adornadowilliam2/vue-vue/blob/master/src/assets/image3.png?raw=true",
        },
        {
          id: 4,
          name: "Image of monk and police rally",
          image: "https://github.com/Adornadowilliam2/vue-vue/blob/master/src/assets/image4.png?raw=true",
        },
        {
          id: 5,
          name: "The holy kick of monk",
          image: "https://github.com/Adornadowilliam2/vue-vue/blob/master/src/assets/image5.png?raw=true",
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
