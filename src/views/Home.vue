<template>
  <v-app>
   <body>
   
    <div id="caro">
      <v-carousel hide-delimiters cycle>
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
    ></v-carousel-item>
  </v-carousel>
    </div>
  
</body>
  </v-app>
</template>

<script>
export default {
    data () {
      return {
        items: [
          {
            src: 'https://www.2trendy.dk/images/topbillede-vans-08-02-19.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
          },
        ],
      }
    },
  }
</script>

<style>


</style>