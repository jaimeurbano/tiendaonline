<template>
    <div style="background-color: #ccffcc;">
        <cabezote
         :productos="comprasrealizadas"
        ></cabezote>

        <manager center
         :productos="productos"
         @compra="compra">
        </manager>  
        <div>DATOS DEL VENDEDOR</div>
      <div>celular: 3203293258</div>
      <div>correo: edjaurba@gmail.com</div>   
    </div>
     
</template>

<script>
import cabezote from '~/components/cabezote.vue'
export default {
  components: { cabezote },
    data() {
        return {
         
          comprasrealizadas : [],
          productos : [
            {
                imagen : 'https://carroya-commons.avaldigitallabs.com/2284403/2284403_19_l.jpg',
                precio :  62990000,
                titulo : 'KIA NIRO',
                descripcion : 'Mazda 3'
            },
             {
                imagen : 'https://carroya-commons.avaldigitallabs.com/2283740/2283740_19_l.jpg',
                precio : 151990000,
                titulo : 'KIA Niro',
                descripcion : 'Automovil 0km modelo 2025',

             } ,
             {
                imagen : 'https://carroya-commons.avaldigitallabs.com/2283729/2283729_1_l.jpg',
                precio : 85970000,
                titulo : 'KIA STONIC',
                descripcion : 'Automovil rojo 0km 2025',

             } ,
             {
                imagen : 'https://carroya-commons.avaldigitallabs.com/2283730/2283730_1_l.jpg',
                precio : 95960000,
                titulo : 'KIA SONET',
                descripcion : 'AUTOMOVIL blanco con negro 0KM 2025',

             } ,
             {
                imagen : 'https://carroya-commons.avaldigitallabs.com/2284076/2284076_4_l.jpg',
                precio : 73970000,
                titulo : 'KIA PICANTO',
                descripcion : 'Sistema de dirección: Asistida Eléctricamente',

             } ,
             {
                imagen : 'https://carroya-commons.avaldigitallabs.com/2283735/2283735_1_l.jpg',
                precio : 118970000,
                titulo : 'KIA SELTOS',
                descripcion : 'Automivil automático color rojo modelo 2025',

             } ,

          ]
            

                               
           
        }
    },
    methods: {
      compra(data){
         this.comprasrealizadas.push(data)
      }
    },
    
}


</script>