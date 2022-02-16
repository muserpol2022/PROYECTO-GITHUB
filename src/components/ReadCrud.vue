<template>
  <div class="contenedor">
    <div class="contenedor-estudiantes">
      <div class="contenedor-tabla">
        <table id="tabla" class="listado-estudiantes">
          <thead>
            <tr>
              <td>nombre</td>
              <td>paterno</td>
              <td>materno</td>
              <td>genero</td>
              <td>nacionalidad</td>
             
            </tr>
          </thead>
          <tbody>
            <tr v-for="estudiante in datos" :key="estudiante">
              <td>{{ estudiante.nombre }}</td>
              <td>{{ estudiante.paterno }}</td>
              <td>{{ estudiante.materno }}</td>
              <td>{{ estudiante.genero }}</td>
              <td>{{ estudiante.nacionalidad }}</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>

<script>
import datosBD from "@/assets/datos.json"; //include
export default {
  data: () => ({
    datos: datosBD,
  }),
};
</script>

<style>

</style>
