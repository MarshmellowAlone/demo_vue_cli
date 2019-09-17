<template>
   <div class="gallery">
      <div class="gallery__item">
         <img :src="url" alt="imagen" class="gallery__image">
         <p class="gallery__description">{{ description }}</p>
      </div>
   </div>
</template>

<script>
   export default {
      name: 'PhotoGallery',
      props: {
         url: String,
         description: {
            type: String,
            default: 'Descripción Foto'
         }
      }
   }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
   .gallery {
      background-color: burlywood;
      padding: 1em;
      margin: .5em;   
   }
</style>
