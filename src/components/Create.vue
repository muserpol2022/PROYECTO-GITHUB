<template>
    <div>
        <button v-on:click="descartar()" >Modificar</button>
        <div v-show="evento">
            <form action="">
                <table>
                    
                    <tr>
                        <td>Nombre(s)</td>
                        <!-- //vmodel para value -->
                        <td><input type="text"   v-model="mod_nombre"></td>
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
                       <td>  <button v-on:click="descartar">Descartar</button> </td>
                       <td> <button v-on:click="imprime()">Guardar</button></td>
                   </tr>
                </table>
            
            </form   >
        
        </div>
       
    </div>
     
                       
                    

</template>

<script>
export default {
    name: "Modificar",
   
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
        
        descartar: function(){

            this.evento = true;
            var a=document.getElementById("")
        },
        guarda: function() {
            this.evento =false;
        },
        imprime: function(){
        
            alert(this.mod_nombre);
        }
        
    }
}
</script>
