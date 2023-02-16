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
    <div class="PageContainer"  :class="{displayNone: onLoad}">
      <div class="gridContainer">
        <Gmap />
        <div class="form">
          <div class="group">
            <div class="item">
              <p class="label">Nom</p>
              <input type="text" placeholder="Doe">
            </div>
            <div class="item">
              <p class="label">Prénom</p>
              <input type="text" placeholder="John">
            </div>
          </div>
          <div class="item">
            <p class="label">E-mail</p>
            <input type="text" placeholder="john.doe@gmail.com">
          </div>
          <div class="item">
            <p class="label">N° de Téléphone</p>
            <input type="text" placeholder="0X.XX.XX.XX.XX">
          </div>
          <div class="item">
            <p class="label">Message</p>
            <textarea name="textarea" />
          </div>
        </div>
      </div>
      <Footer />
    </div>
  </div>
</template>

<style scoped>
  @import url('../assets/css/index.css');
  @import url('./contact.css');
</style>