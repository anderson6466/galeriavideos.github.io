<template>
 <div>
 
 
 <v-toolbar  flat  dark    >

<v-app-bar-nav-icon     @click.stop="drawer = !drawer"   style=" color:#FFFFFF;"       ></v-app-bar-nav-icon>
<v-toolbar-title    class="font-weight-light"   >

<img src="https://caseros.herokuapp.com/xvideos.png"    />


</v-toolbar-title>

 
 
<v-spacer ></v-spacer >
<div  style="text-align:left;align-content:left;position:left;">

<v-layout  flat   >
    <v-flex v-if="persona.user==null">
    <v-btn  style="background:#80B471;margin:8px; color:#FFFFFF; "    >Ingreso</v-btn>
       </v-flex>
 
        <v-flex v-else >
     <v-btn    style="background:red;margin:8px; color:#FFFFFF;" >Salir</v-btn>
    </v-flex>

 


   <v-autocomplete
    
   
  
 
      cache-items
      class="mx-4"
     
   
      hide-details
      label="Buscas algo?"
      solo-inverted
    ></v-autocomplete>
 <v-btn icon>
      <v-icon>mdi-magnify</v-icon>
    </v-btn>

</v-layout>
</div>

</v-toolbar>
 


 
 
 
 </div>
</template>

<script>
  export default {
    name: 'HelloWorld',

   data () {
      return {
        drawer: null,
        bsalir: false,
      persona:{
        nombre:null,
        dni:null,
        password:null,
        user:null,
        

      },

        items: [
          { title: 'Home', icon: 'mdi-view-dashboard' },
          { title: 'About', icon: 'mdi-forum' },
        ],
      }
    },





 
    
    
    
  }
</script>
