<template>
    <div>
      <header>
        <div class="logo">Hotel</div>
        <nav>
          <ul class="nav-links">
            <li><a href="#about">NOSOTROS</a></li>
            <li><a href="#rooms">HABITACIONES</a></li>
            <li><a href="#services">SERVICIOS</a></li>
            <li><a href="#gallery">GALERÍA</a></li>
            <li><a href="#contact">CONTACTO</a></li>
          </ul>
        </nav>
      </header>
  
      <section class="hero">
        <h1>Bienvenido a las Mil Noches</h1>
        <p>Un refugio de lujo y confort</p>
        <button @click="reservar" class="btn">RESERVA</button>
      </section>
  
      <section id="about" class="content">
        <h2>Sobre Nosotros</h2>
        <p class="Bienvenida">Bienvenido a Hotel Mil Noches</p>
        <p class="informacion">Un destino donde la elegancia, la comodidad y el servicio excepcional se combinan...</p>
        <p class="historia">¡Déjanos ser parte de tu historia!</p>
      </section>
  
      <section id="rooms" class="content">
        <h2>Habitaciones</h2>
        <p>Explora nuestras habitaciones diseñadas para tu comodidad.</p>
        <div id="carouselExample" class="carousel slide">
          <div class="carousel-inner">
            <div v-for="(habitacion, index) in habitaciones" :key="index" class="carousel-item" :class="{ active: index === 0 }">
              <img :src="habitacion.imagen" alt="Habitación">
              <h2>{{ habitacion.titulo }}</h2>
              <p>{{ habitacion.descripcion }}</p>
              <button class="price-button" @click="mostrarPrecio(index)">{{ habitacion.boton }}</button>
            </div>
          </div>
        </div>
      </section>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        habitaciones: [
          { imagen: 'Img/Individual.jpg', titulo: 'Habitación Estándar', descripcion: 'Cómoda habitación...', boton: 'Buy Now', precio: '$80 USD' },
          { imagen: 'Img/2persona.jpg', titulo: 'Habitación Doble', descripcion: 'Espaciosa habitación...', boton: 'Buy Now', precio: '$120 USD' },
          { imagen: 'Img/vip.jpg', titulo: 'Habitación VIP', descripcion: 'Lujosa suite...', boton: 'Comprar', precio: '$200 USD' }
        ]
      };
    },
    methods: {
      reservar() {
        alert('Reserva iniciada');
      },
      mostrarPrecio(index) {
        this.habitaciones[index].boton = this.habitaciones[index].precio;
      }
    }
  };
  </script>
  
  <style>
  .logo {
    font-size: 24px;
    font-weight: bold;
  }
  .nav-links {
    display: flex;
    gap: 15px;
    list-style: none;
  }
  .hero {
    text-align: center;
    padding: 50px;
    background: #f5f5f5;
  }
  .carousel-item img {
    width: 100%;
    height: auto;
  }
  </style>
  