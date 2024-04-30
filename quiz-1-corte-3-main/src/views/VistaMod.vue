<template>
    <ion-page>
      <ion-header>
        <ion-toolbar>
          <ion-title>Módulo: {{ modulo.nombre }}</ion-title>
        </ion-toolbar>
      </ion-header>
      <ion-content>
        <ComponenteRepetido
          :nombre="modulo.nombre"
          :descripcion="modulo.descripcion"
          :codigo="modulo.codigo"
          :estado="modulo.estado"
        />
        <p>Ruta: {{ modulo.ruta }}</p>
      </ion-content>
    </ion-page>
  </template>
  
  <script>
  import ComponenteRepetido from './ComponenteRepetido.vue';
  
  export default {
    props: {
      modulo: Object
    },
    components: {
      ComponenteRepetido
    }
  };
  </script>