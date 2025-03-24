<script setup>
//importacion del card principal
import CardPrincipal from './CardPrincipal.vue';
//importacion del primer card
import Card from './Card.vue';
</script>

<template>
  <div class="container">
    <h1 class="text-center">Gym Tlaxiaco 7w7</h1>
    
    <!-- Primer row -->
   <CardPrincipal/>
    
    <!-- Segundo row -->
   <Card/>
    
    <!-- Tercer row centrado -->
    <div class="row mt-4 justify-content-center">
      <div class="col-md-4">
        <div class="card">
          <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ9lOD8fZLTzoSSHja7uB8uZuConInXOA9Tiw&s"  class="card-img-top img-fluid rounded mx-auto d-block" 
     style="max-width: 300px; max-height: 200px;" 
     alt="Ejercicio en gimnasio">
          <div class="card-body text-center">
            <p class="card-text">Dietas para una vida saludable y un mejor endimeinto.</p>
            <button class="btn btn-warning">Mas informacion aqui</button>
          </div>
        </div>
      </div>
      <div class="col-md-4">
        <div class="card">
          <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTuRYvHXXOO2wkiFKi-EHATSUZV-N0CAh_iNQ&s" 
     class="card-img-top img-fluid rounded mx-auto d-block" 
     style="max-width: 300px; max-height: 200px;" 
     alt="Ejercicio en gimnasio">

          <div class="card-body text-center">
            <p class="card-text">Mensualidad de gymnasisos,precios y mas.</p>
            <button class="btn btn-warning">Mas informacion aqui</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

