<template>
   <div class="carduser__item">
      <img :src="photo" width="50" height="50" alt="imagen" class="carduser__image">
      <span class="carduser_name">{{ fullName }}</span>
      <a class="carduser__link" :href="email">{{ username }} - {{ email }}</a>
      <p class="carduser__description">{{ description }}</p>
   </div>
</template>

<script>
   export default {
      name: 'CardUser',
      props: {
         name: { 
            type: String,
            default: 'Nombre Usuario'
         },
         username: { 
            type: String,
            default: 'user'
         },
         email: { 
            type: String,
            default: 'email',
         },
         photo: { 
            type: String,
            default: 'https://loremflickr.com/320/240'
         },
         description: {
            type: String,
            default: 'Descripción Usuario'
         },
         fullName: {
            type: String,
            default: 'Nombre usuario'
         },
      },
   }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
   .carduser__item {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      margin: 1.5em 0;
   }
   
</style>
