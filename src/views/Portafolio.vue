<template>
   <div class="portafolio">
      <h2>Página Portafolio</h2>
      <CardUser  
         v-for="(user, index) in users" 
         :key="index" 
         :username="user.username" 
         :email="user.email" 
         :photo="user.photo" 
         :description="user.description" 
         :fullName="user.fullName"
      />   
   </div>
</template>

<script>
// @ is an alias to /src
import CardUser from '@/components/CardUser.vue';
import axios from 'axios';

export default {
   name: 'portafolio',
   components: {
      CardUser
   },
   data() {
      return {
         users: [],
         errors: [],
      }
   },
   beforeCreate() {
      console.log("Antes de crear")
   },
   created() {
      console.log( "Obtener Datos" );
      axios.get( 'https://randomuser.me/api/?results=5' )
         .then( response => this.users = response.data.results.map(
            user => {
               return {
                  username: user.login.username,
                  fullName: `${user.name.title}: ${user.name.first} ${user.name.last}`,
                  email: user.email,
                  photo: user.picture.medium,
                  description: 'Descripcion',
               }
            }
         ))
         .catch( e => {
            this.errors.push( e )
         });
      console.log( "Finalizado la obtención de datos" );
   },
   beforeMount() {
      console.log( "Antes de añadir al DOM" );
   },
   mounted() {
      console.log( `${this.users}` );
      console.log( "Componente añadido al DOM" );
   },
   
}
</script>
