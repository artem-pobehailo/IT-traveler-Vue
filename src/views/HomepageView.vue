<script setup lang="ts">
import IButton from '../components/IButton/IButton.vue'
</script>

<template>
  <main class="flex h-screen">
    <section class="flex-1 flex justify-center items-center px-5 bg-[#f3743d]">
      <div class="text-white text-center">
        <img class="inline mb-6" src="../assets/img/map-pin.svg" alt="" />
        <h1 class="font-bold text-4xl mb-7">IT traveler</h1>
        <p class="leading-6 mb-11 max-w-127">
          Простий і зручний веб додаток, який дозволить тобі <br />
          відмічати твої улюблені місця, а також ті, в яких би ти дуже <br />
          хотів побувати. Тож не зволікай і спробуй сам.
        </p>
        <IButton></IButton>
        <div class="flex mt-8">
          <p>У вас ще немає аккаунту?</p>
          <p>Зареєструватися або увійти</p>
        </div>
      </div>
    </section>
    <section class="flex-1">
      <img class="h-full w-full object-cover" src="../assets/img/static-map.png" alt="" />
    </section>
  </main>
</template>
