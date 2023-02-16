<template>
    <nav>
        <ul class="left">
            <li>
                <NuxtLink to="/">
                    Accueil
                </NuxtLink>
            </li>
            <li>
                <NuxtLink to="/Magasin">
                    Magasin
                </NuxtLink>
            </li>
            <li>
                <NuxtLink to="/Atelier">
                    Atelier
                </NuxtLink>
            </li>
            <li>
                <NuxtLink to="/Contact">
                    Contact
                </NuxtLink>
            </li>
        </ul>
        <div class="center">
            <img src="../assets/img/logo.png" alt="logo Muscle Car Loc">
        </div>
        <ul class="right">
            <li>
                <NuxtLink to="/Dashboard">
                    <i class="fa-solid fa-user"></i>
                </NuxtLink>
            </li>
            <li>
                <i class="fa-solid fa-basket-shopping"></i>
            </li>
        </ul>
        <slot />
    </nav>
</template>

<style scoped>
    @import url('./default.css');
</style>