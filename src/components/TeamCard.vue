<template>
        <div>
          <div>
              <img v-bind:src="miembro.image" class="card-img-top rounded-circle" alt="">
          </div>  
          <div class="card-body text-justify text-center">
            <h4>
              {{"Miembro: "+miembro.codigo}}
            </h4>
            <h4>
              {{"Rol: "+miembro.rol}}
            </h4>
            <h4 class="p-3">
              {{miembro.nombre}}
            </h4>
            <h5>
              {{miembro.descripcion}}
            </h5>
          </div>
        </div>
</template>

<script>

    export default {
        name: "TeamCard",
        //props: ['miembro', 'rol', 'nombre', 'texto', 'url']
        props:['miembro']
            
    }
</script>

<style scoped>
    img{
        display:block;
        height:300px;
        width:auto;
        margin-left:auto;
        margin-right:auto;
    }
</style>
