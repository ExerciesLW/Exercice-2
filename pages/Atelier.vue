<script setup>
  import { ref } from 'vue';
  let onLoad = ref(true);

  setTimeout(() => { onLoad.value = false;}, "2700");
</script>

<template>
  <div>
    <NuxtLayout />
    <div class="Loading" :class="{displayNone: !onLoad}">
      <Loading />
    </div>
    <div class="PageContainer" :class="{displayNone: onLoad}">
      <header>
        <div>
          <img src="../assets/img/painter.png" alt="painter">
        </div>
        <div>
          <h1>Besoin d'un design unique pour un véhicule unique ?</h1>
          <h1>Nos Ateliers ont l'expertise qu'il vous faut</h1>
        </div>
      </header>
      <section class="covering">
        <div>
          <img src="../assets/img/covering.jpg" alt="">
        </div>
        <div>
          <h2>Covering</h2>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Id facilis maiores eius quaerat ad laboriosam, modi error rerum blanditiis pariatur? Nesciunt quibusdam iste, corrupti neque in magni provident vero nobis natus nulla magnam ipsum dignissimos incidunt voluptatum consequatur expedita. Cupiditate mollitia velit corrupti ipsum laboriosam recusandae quas eum consequuntur, itaque quasi. Nemo dolor exercitationem voluptates, necessitatibus quidem labore molestiae iste!
          </p>
        </div>
      </section>
      <section class="peintures">
        <div>
          <img src="../assets/img/paiting.jpg" alt="">
        </div>
        <div>
          <h2>Peinture</h2>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Id facilis maiores eius quaerat ad laboriosam, modi error rerum blanditiis pariatur? Nesciunt quibusdam iste, corrupti neque in magni provident vero nobis natus nulla magnam ipsum dignissimos incidunt voluptatum consequatur expedita. Cupiditate mollitia velit corrupti ipsum laboriosam recusandae quas eum consequuntur, itaque quasi. Nemo dolor exercitationem voluptates, necessitatibus quidem labore molestiae iste!
          </p>
        </div>
      </section>
      <section class="carrosserie">
        <div>
          <img src="../assets/img/carrosserie.jpg" alt="">
        </div>
        <div>
          <h2>Carrosserie</h2>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Id facilis maiores eius quaerat ad laboriosam, modi error rerum blanditiis pariatur? Nesciunt quibusdam iste, corrupti neque in magni provident vero nobis natus nulla magnam ipsum dignissimos incidunt voluptatum consequatur expedita. Cupiditate mollitia velit corrupti ipsum laboriosam recusandae quas eum consequuntur, itaque quasi. Nemo dolor exercitationem voluptates, necessitatibus quidem labore molestiae iste!
          </p>
        </div>
      </section>
      <section class="interieur">
        <div>
          <img src="../assets/img/interior.png" alt="">
        </div>
        <div>
          <h2>Intérieur</h2>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Id facilis maiores eius quaerat ad laboriosam, modi error rerum blanditiis pariatur? Nesciunt quibusdam iste, corrupti neque in magni provident vero nobis natus nulla magnam ipsum dignissimos incidunt voluptatum consequatur expedita. Cupiditate mollitia velit corrupti ipsum laboriosam recusandae quas eum consequuntur, itaque quasi. Nemo dolor exercitationem voluptates, necessitatibus quidem labore molestiae iste!
          </p>
        </div>
      </section>
      <section class="mecanique">
        <div>
          <img src="../assets/img/mecanics.jpg" alt="">
        </div>
        <div>
          <h2>Mécanique</h2>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Id facilis maiores eius quaerat ad laboriosam, modi error rerum blanditiis pariatur? Nesciunt quibusdam iste, corrupti neque in magni provident vero nobis natus nulla magnam ipsum dignissimos incidunt voluptatum consequatur expedita. Cupiditate mollitia velit corrupti ipsum laboriosam recusandae quas eum consequuntur, itaque quasi. Nemo dolor exercitationem voluptates, necessitatibus quidem labore molestiae iste!
          </p>
        </div>
      </section>
      <Footer />
    </div>
  </div>
</template>

<style scoped>
  @import url('../assets/css/index.css');
  @import url('./atelier.css');
</style>