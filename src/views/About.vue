<template>
   <div class="about">
      <h1>Está es la página about</h1>
      <img :src="url" />
   </div>
</template>

<script>
export default {
   name: 'about',
   data() {
      return {
         url: 'https://loremflickr.com/320/240'   
      }
   },
}
</script>
