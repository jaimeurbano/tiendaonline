<template>
    <v-dialog
      v-model="mostrar"
      width="auto"
      persistent
    >
      <v-card
        max-width="400"
        prepend-icon="mdi-update"
        title="Productos Comprados"
      >

      <v-card-text>
        <table border="1">
          <thead>
      <th>Producto</th>
      <th>Cantidad</th>
      <th>Precio</th>
      <th>descripción</th>
      
  </thead><tbody>
    <tr v-for="data in compras">
        <td>{{ data.titulo }}</td>
        <td>{{ data.cantidad }} 1 </td>
        <td>{{ data.precio }}</td>
        <td>{{ data.descripcion }}</td>
      </tr>
    </tbody>
  
        </table>
      
        </v-card-text>

        <template v-slot:actions>
          <v-btn
            class="ms-auto"
            text="Cerrar"
            @click="cerrar()"
          ></v-btn>
        </template>
      </v-card>
    </v-dialog>
   
</template>

<script>

export default {
    props: {
    show: {
        type: Boolean,
        default: false
    },
    compras: {
        type: Array,
       
    },
},
data() {
        return {
            mostrar : false      
          }
    },
    methods:{
        cerrar(){
         this.$emit('cerrar')
      }
    },
 watch:{
    show(){
        console.log('awi')
        this.mostrar = this.show
    }
 }   
}
</script>