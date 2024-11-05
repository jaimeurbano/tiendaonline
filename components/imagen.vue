<template>
    <div>
     <h1>{{titulo}}</h1>
     <img :style="{ width : ancho + 'px', height : alto + 'px' }"
     :src="img">
    </div>
    <div class="image-container">
        <img :src="imageSrc" alt="Imagen centrada" />
    </div>
</template>

<script>
import Producto from './producto.vue';

export default {
    props: {
        titulo : String,
        img: String,
        ancho:Number,
        alto:Number
   
  }
}
</script>
