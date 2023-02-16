<script setup>
  import { ref } from 'vue';
  import Categories from '../data/Catégories.json';
  

  let categorie_selected = ref('');
  let categorie_returned = ref(categorie_selected.value);


  let allList =[
            "Ghostbuster",
            "Scoubidoo",
            "Retour vers le Futur",
            "Choupette",
            "Boulevard de la Mort",
            "Bullit",
            "James Bond - GoldFinger",
            "Taxi",
            "Fast & Furious",
            "Christine",
            "Stranger Things",
            "Magnum",
            "K2000",
            "Supernatural",
            "Alerte Cobra",
            "Sherif Fais Moi Peur",
            "Amicalement Votre",
            "Agence Tout Risque",
            "Breaking Bad",
            "Starsky et Hutch"
  ]
  let filmsList = [
            "Ghostbuster",
            "Scoubidoo",
            "Retour vers le Futur",
            "Choupette",
            "Boulevard de la Mort",
            "Bullit",
            "James Bond - GoldFinger",
            "Taxi",
            "Fast & Furious",
            "Christine"
        ];
  let seriesList = [
            "Stranger Things",
            "Magnum",
            "K2000",
            "Supernatural",
            "Alerte Cobra",
            "Sherif Fais Moi Peur",
            "Amicalement Votre",
            "Agence Tout Risque",
            "Breaking Bad",
            "Starsky et Hutch"
        ];

  let isFilm = ref(false);
  let isSerie = ref(false);
  let isAll = ref(true);

  const changeValue = (e) => {
    let newValue = e.target.value;
    categorie_selected.value = newValue;
    if(newValue === ""){
      isFilm.value = false;
      isSerie.value = false;
      isAll.value = true;
    }
    if(newValue === "Films"){
      isFilm.value = true;
      isSerie.value = false;
      isAll.value = false;
    }
    if(newValue === "Séries"){
      isFilm.value = false;
      isSerie.value = true;
      isAll.value = false;
    }
  }

  let onLoad = ref(true);

  setTimeout(() => { onLoad.value = false;}, "2700");
</script>

<template>
  <NuxtLayout />
  <div class="Loading" :class="{displayNone: !onLoad}">
    <Loading />
  </div>
  <div class="PageContainer" :class="{displayNone: onLoad}">
    <ul>
      <li>
        <p>Type de Véhicule :</p>
        <div class="select">
          <select :value="categorie_selected" @change="changeValue">
            <option value="">Tous</option>
            <option v-for="categorie in Categories" :value="categorie.name">{{categorie.name}}</option>
          </select>
        </div>
      </li>
      <li>
        <p>Film :</p>
        <div :class="{selectDisabled : !isFilm && !isAll, select : isFilm || isAll}">
          <select :disabled="!isFilm && !isAll">
            <option value="">Tous</option>
            <option v-for="film in filmsList" :value="film">{{film}}</option>
          </select>
        </div>
      </li>
      <li>
        <p>Série :</p>
        <div :class="{selectDisabled : !isSerie && !isAll, select : isSerie || isAll}">
          <select :disabled="!isSerie && !isAll">
            <option value="">Tous</option>
            <option v-for="serie in seriesList" :value="serie">{{serie}}</option>
          </select>
        </div>
      </li>
    </ul>
    <section class="List" :class="{displayNone : !isAll}">
      <div v-for="el in allList" data-name="{{ el }}">
        <img src="../assets/img/placeholderV.png" alt="">
        <h2>{{ el }}</h2>
        <NuxtLink to="/Product">Détails</NuxtLink>
      </div>
    </section>
    <section class="List" :class="{displayNone : !isFilm}">
      <div v-for="film in filmsList" data-name="{{ film }}">
        <img src="../assets/img/placeholderV.png" alt="">
        <h2>{{ film }}</h2>
        <NuxtLink to="/Product">Détails</NuxtLink>
      </div>
    </section>
    <section class="List" :class="{displayNone : !isSerie}">
      <div v-for="serie in seriesList" data-name="{{ serie }}">
        <img src="../assets/img/placeholderV.png" alt="">
        <h2>{{serie}}</h2>
        <NuxtLink to="/Product">Détails</NuxtLink>
      </div>
    </section>
    <Footer />
  </div>
</template>

<style>
  @import url('../assets/css/index.css');
  @import url('./magasin.css');
</style>