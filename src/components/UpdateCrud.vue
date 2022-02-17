<template>
    <div>
        <button v-on:click="modificar(datos)" >Modificar</button>
        <div v-show="evento">
            <form action="">
                <table>
                    <tr>
                        <td>ID</td>
                        <td><span id="mod_id">{{datos.id}}</span></td>
                    </tr>
                    <tr>
                        <td>Nombre(s)</td>
                        <td><input type="text"  id="mod_nombre" value=""></td>
                     </tr>
                    <tr>
                        <td>Paterno</td>
                        <td><input type="text"  id="mod_paterno"></td>
                     </tr>
                    <tr>
                        <td>Materno</td>
                         <td><input type="text"  id="mod_materno"></td>
                     </tr>
                    <tr>
                        <td>Género</td>
                        <td><input type="text"  id="mod_genero"></td>
                     </tr>
                    <tr>
                        <td>Nacionalidad</td>
                        <td><input type="text"  id="mod_nacionalidad"></td>
                    </tr>
                    <tr>
                        <td><button v-on:onclick="descartar">Descartar</button></td>
                        <td><button v-on:onclick="guardar">Guardar</button></td>
                    </tr>
                </table>
            </form>
        </div>
    </div>
    

</template>

<script>
export default {
    name: "Modificar",
    props:[
        "id_estudiante",
        "datos"
    ],
    data(){
        return{
            evento: false,
            mod_id: "",
            mod_nombre: "",
            //mod_paterno: "",
            //mod_materno: "",
            //mod_genero: "",
            //mod_nacionalidad: ""
        }
    },
    methods:{
        modificar: function(datos){
            this.mod_id = datos.id;
            this.mod_nombre = datos.nombre;
            //this.mod_paterno = datos.paterno;
            //this.mod_materno = datos.materno;
            //this.mod_genero = datos.genero;
            //this.mod_nacionalidad = datos.nacionalidad;
            this.evento = true;

        },
        descartar: function(){

            this.evento = false;
        }
        
    }
}
</script>
