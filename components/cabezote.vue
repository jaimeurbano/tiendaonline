<template>
    <div>
      <v-toolbar
        image="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTDE2Kxk0IYLnoP2RKTZR89VtNi51S0Jt-AMQ&s"
        dark
        height="150"
      >
        <v-app-bar-nav-icon></v-app-bar-nav-icon>
  
        <v-toolbar-title  
        ><h1>AUTOMOVILES</h1></v-toolbar-title>
  
        <v-spacer></v-spacer>
  
        <carrito class="mr-5"
         :productos="productos"
        >

        </carrito>
      </v-toolbar>
      
    </div>
  </template>
  <script>
  export default {
    props:{
      productos : Array,
    }
  }
  </script>
  <style scoped>
   
  </style>