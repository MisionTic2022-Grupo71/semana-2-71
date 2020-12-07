<template>
        <div>
          <div>
              <img v-bind:src="member.image" class="card-img-top rounded-circle" alt="">
          </div>  
          <div class="card-body text-justify text-center">
            <h4>
              {{"Miembro: "+member.codigo}}
            </h4>
            <h4>
              {{"Rol: "+member.rol}}
            </h4>
            <h4 class="p-3">
              {{member.nombre}}
            </h4>
            <h5>
              {{member.descripcion}}
            </h5>
          </div>
        </div>
</template>

<script>

    export default {
        name: "TeamCard",
        //props: ['miembro', 'rol', 'nombre', 'texto', 'url']
        props:['member']
            
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
