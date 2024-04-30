<template>
    <ion-page>
      <ion-header>
        <ion-toolbar>
          <ion-title>Rol: {{ rol.nombre }}</ion-title>
        </ion-toolbar>
      </ion-header>
      <ion-content>
        <ComponenteRepetido
          :nombre="rol.nombre"
          :descripcion="rol.descripcion"
          :codigo="rol.codigo"
          :estado="rol.estado"
        />
      </ion-content>
    </ion-page>
  </template>
  
  <script>
  import ComponenteRepetido from './ComponenteRepetido.vue';
  
  export default {
    props: {
      rol: Object
    },
    components: {
      ComponenteRepetido
    }
  };
  </script>