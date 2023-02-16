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
            <img src="../assets/img/car.png" alt="">
        </div>
        <div>
            <h1>Il n'y a pas que votre acteur préféré qui peut la conduire</h1>
            <NuxtLink to="/Magasin"></NuxtLink>
        </div>
      </header>
      <section class="location">
        <div>
            <img src="../assets/img/map.png" alt="Location Muscle Car Loc">
        </div>
        <div>
            <h2>Présent à nice, mais livraison possible à l'échelle nationale</h2>
            <p>
                Lorem ipsum dolor sit, amet consectetur adipisicing elit. Possimus dolore aliquid quo vitae, sequi blanditiis harum obcaecati, velit laboriosam modi eveniet voluptatem ipsam fugit minima dolores, vero dolor animi! Deleniti, architecto doloribus! Consectetur, alias. Non ducimus doloremque, inventore officia illum laudantium a numquam perspiciatis temporibus deleniti error, ad facere unde in! Odio voluptatum assumenda sunt repellendus quis debitis accusantium beatae!
            </p>
        </div>
      </section>
      <section class="deadline">
        <div>
            <h2>Flexible, Comme vos envies</h2>
            <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Quasi, recusandae et nam incidunt ea minus cum aliquid veniam quis vitae similique id, voluptatibus vero voluptatum! Repudiandae commodi obcaecati in, unde, magni, vero consectetur mollitia ipsum culpa dicta amet. Libero atque voluptas distinctio recusandae nesciunt. Necessitatibus iusto cum quas. Rerum iste quisquam soluta sed delectus vitae. Vero obcaecati exercitationem in accusantium.
            </p>
        </div>
        <div>
            <img src="../assets/img/Calendar.png" alt="Calendrier">
        </div>
      </section>
      <Footer />
    </div>
  </div>
</template>

<style scoped>
  @import url('../assets/css/index.css');
  @import url('./index.css');

</style>