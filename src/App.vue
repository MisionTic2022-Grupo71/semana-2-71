<template>
  <div id="app">
    <header id="home">
      <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <a class="navbar-brand" href="#home">Sprint 2</a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav ml-auto mr-auto">
            <li class="nav-item active">
              <a class="nav-link" href="#home">Inicio <span class="sr-only">(current)</span></a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#news">Noticias</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#team">Equipo</a>
            </li>
          </ul>
        </div>
      </nav>

      <div id="carouselExampleControls" class="carousel slide" data-ride="carousel">
        <div class="carousel-inner">
          <div class="carousel-item active">
            <img src="https://aprendelibvrefiles.blob.core.windows.net/aprendelibvre-container/course/informatica_basica/image/compescritorio-01_xl.png" class="d-block w-100" style="height:700px; width:auto;" alt="...">
          </div>
          <div class="carousel-item">
            <img src="https://concepto.de/wp-content/uploads/2014/08/programacion-2-e1551291144973.jpg" class="d-block w-100" style="height:700px; width:auto;" alt="...">
          </div>
          <div class="carousel-item">
            <img src="https://blog.educacionit.com/wp-content/uploads/2018/09/shutterstock-10338536170938-620x354-01-750x410.jpg" class="d-block w-100" style="height:700px; width:auto;" alt="...">
            </div>
        </div>
        <a class="carousel-control-prev" href="#carouselExampleControls" role="button" data-slide="prev">
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="sr-only">Previous</span>
        </a>
        <a class="carousel-control-next" href="#carouselExampleControls" role="button" data-slide="next">
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="sr-only">Next</span>
        </a>
      </div>
    </header>
    <main>
      <div id="news" class="navbar navbar-dark bg-dark m-3 rounded-pill">
        <span class="text-white ml-auto mr-auto">
          <h3>
              Noticias
          </h3>         
        </span>
      </div>
      <noticia-api></noticia-api>

      <div id="team" class="navbar navbar-dark bg-dark m-3 rounded-pill">
        <span class="text-white ml-auto mr-auto">
          <h3>
              Equipo
          </h3>         
        </span>
      </div>

      <div class="card-deck">
        <div class="card col-4" v-for="(nmiembro, index) of  team" :key="index">
          <team-card 
          v-bind:miembro="nmiembro">
            
          </team-card>
        </div>
      </div>

    </main>
        <!-- Footer -->
    <footer class="page-footer font-small teal pt-4 bg-dark text-white mt-3">

      <!-- Footer Text -->
      <div class="container-fluid text-center text-md-left">

        <!-- Grid row -->
        <div class="row">

          <!-- Grid column -->
          <div class="col-md-6 mt-md-0 mt-3">

            <!-- Content -->
            <h5 class="text-uppercase font-weight-bold">Repositorio</h5>
            <p>Desarrollando sprint 2!!</p>
            <a href="https://github.com/MisionTic2022-Grupo71/semana-2-71.git"><p>https://github.com/MisionTic2022-Grupo71/semana-2-71.git</p></a>

          </div>
          <!-- Grid column -->

          <hr class="clearfix w-100 d-md-none pb-3">

          <!-- Grid column -->
          <div class="col-md-6 mb-md-0 mb-3">

            <!-- Content -->
            <h5 class="text-uppercase font-weight-bold">Contacto</h5>
                <p>Juan Pablo Caycedo Hernandez - jpcaycedo@gmail.com</p>
                <p>Daniel Galvez Zuluaga - dannytrompeta@gmail.com</p>
                <p>Roque Alexander Pineda - rpinedac@ibero.edu.co</p>



          </div>
          <!-- Grid column -->

        </div>
        <!-- Grid row -->

      </div>
      <!-- Footer Text -->

      <!-- Copyright -->
      <div class="footer-copyright text-center py-3 bg-secondary text-primary">© 2020 Copyright:
        <a href="https://mdbootstrap.com/"> Sprint 2</a>
      </div>
      <!-- Copyright -->

    </footer>
    <!-- Footer -->
  </div>
</template>

<script>

import NoticiaApi from './components/NoticiaApi.vue'
import TeamCard from './components/TeamCard.vue'

export default {
  components: { TeamCard, NoticiaApi },
  name: 'App',
  data(){
    return{
      team:[{
        codigo: 1,
        nombre: 'Juan Pablo Caycedo Hernandez',
        descripcion: 'Tengo 22 años, estudio ingenieria mecanica en la Universidad Nacional sede Bogota, y mis pasatiempos son tocar la guitarra y hacer ejercicio',
        rol: 'Scrum Master',
        image: require('./assets/juan.jpg')
      },
      {
        codigo: 2,
        nombre: 'Daniel Galvez Zuluaga',
        descripcion: 'Tengo 26 años, Estudio Ingenieria Electronica en la Universidad Nacional sede manizales, y de pasatiempo imagino que son los hobbies asi que jugar videojuegos y ver series.',
        rol: 'Desarrollador Backend',
        image:require('./assets/daniel.jpeg')
      },
      {
        codigo: 3,
        nombre: 'Roque Alexander Pineda',
        descripcion: 'soy Profesor de Diseño Asistido por Computador en un colegio en la ciudad de Tocancipá,  me gusta jugar  futbol y la tecnología aplicada a la educación.',
        rol: 'Desarrollador Frontend',
        image: require('./assets/alexander.jpeg')
      }]

    }
  }
}


</script>

