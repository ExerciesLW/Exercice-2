<script setup>
    let onLoad = ref(true);

    setTimeout(() => { onLoad.value = false;}, "2700");
</script>

<template>
    <NuxtLayout />
    <div class="Loading" :class="{displayNone: !onLoad}">
        <Loading />
    </div>
    <div class="PageContainer">
        <div class="Container">
            <div>
                <img src="../assets/img/placeholderV.png" alt="">
            </div>
            <div>
                <span>
                    <h1>Modèle</h1>
                    <p>XXXXXXXXX</p>
                </span>
                <span>
                    <h1>Film / Série</h1>
                    <p>XXXXXXXXXXXXXXX</p>
                </span>
                <span>
                    <h1>Tarif Horaire</h1>
                    <p>xx.xx€ / heures</p>
                    <p>Forfait Journée : xx.xx€</p>
                </span>
            </div>
        </div>
        <div class="Description">
            <h1>Description</h1>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sunt, iure? Inventore iure minima, facilis laboriosam vitae dignissimos doloremque. Fugit necessitatibus itaque ut error ab atque alias autem eius facilis similique repudiandae sit nobis et obcaecati eligendi, possimus aliquid quod omnis consectetur quibusdam! Eligendi nobis mollitia rerum! Veritatis quo non dolorum voluptate optio consectetur dolore facilis nam quibusdam aspernatur praesentium nobis ullam enim, soluta ducimus, neque rerum dolores perspiciatis dolorem maiores accusantium iure atque. Facilis facere at quo tempora laborum possimus optio eos minus obcaecati fugiat cupiditate eligendi accusamus ab unde, consequuntur veniam consequatur exercitationem vel molestias molestiae, dolorum a, enim reiciendis! Expedita quae ducimus sequi quasi quo rerum, facilis esse! Aut consequatur nihil quaerat, quia amet, vero neque a corporis possimus sunt consequuntur fugit optio? Aspernatur, dolore autem et voluptatem a vero? Quisquam accusamus repellendus aut eum? Alias vero eos beatae sequi? Ut consequatur quis iusto a ipsam amet eum deserunt maiores suscipit mollitia nihil, sit ipsum magni voluptas? Odit!</p>
        </div>
        <Footer />
    </div>
</template>

<style scoped>
    @import url('../assets/css/index.css');
    @import url('./product.css');
</style>