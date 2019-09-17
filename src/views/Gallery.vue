<template>
   <div class="gallery">
      <h1>Esta es la sección de la galeria</h1>
      <div class="gallery__container">
         <PhotoGallery url="https://loremflickr.com/320/240?random=1" description="Está es la descripción de la imagen 1"/>
         <PhotoGallery url="https://loremflickr.com/320/240?random=2" description="Está es la descripción de la imagen 2"/>
         <PhotoGallery url="https://loremflickr.com/320/240?random=3" description="Está es la descripción de la imagen 3"/>
         <PhotoGallery url="https://loremflickr.com/320/240?random=4" description="Está es la descripción de la imagen 4"/>
         <PhotoGallery url="https://loremflickr.com/320/240?random=5" description="Está es la descripción de la imagen 5"/>
      </div>
   </div>
</template>

<script>
// @ is an alias to /src
import PhotoGallery from '@/components/PhotoGallery.vue'

export default {
   name: 'gallery',
   components: {
      PhotoGallery
   }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
   .gallery__container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      align-items: center;
   }
</style>