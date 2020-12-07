<template>
  <div class="row row-cols-1 row-cols-md-2 ml-3 mr-3">
        <div class="col mb-4" v-for="(item,index) of noticias" :key="index">
          <div class="card h-100">
            <img v-bind:src="item.urlToImage" class="card-img-top" alt="...">
            <div class="card-body">
              <a v-bind:href="item.url"><h5 class="card-title">{{item.title}}</h5></a>
              <p class="card-text">{{item.description}}</p>
            </div>
          </div>
        </div>
  </div>  
</template>

<script>
    import axios from "axios";
    export default {
        name: "NoticiaApi",
        data(){
            return{
                
                noticias:null,
                

            }
        },
        mounted(){
            axios
                .get('http://newsapi.org/v2/top-headlines?country=co&apiKey=63c0ac96cf4c48f4b8f85778ba632624')
                .then(response =>{
                    (this.noticias = response.data.articles.slice(1,5))
                    });
        }
    }
</script>

<style scoped>
    img{
      height:300px;
      width:auto;
    }
</style>
