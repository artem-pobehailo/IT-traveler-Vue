<script setup>
import FavoritePlace from '../FavoritePlace/FavoritePlace.vue'
import IButton from '../IButton/IButton.vue'
import { ref } from 'vue'

const buttonVariant = ref('gradient')

const changeButton = () => {
  buttonVariant.value = buttonVariant.value === 'gradient' ? 'outlined' : 'gradient'
}
</script>

<template>
  <div class="px-6 text-[#000]">
    <div class="text-[rgba(44,44,44,0.5)] mb-4">Додані маркери ({{ counter }})</div>

    <slot name="label"></slot>
    <slot name="list"> </slot>
    <FavoritePlace />

    <slot></slot>
    <IButton class="w-full mt-10" :variant="buttonVariant" @click="changeButton">
      Додати маркер
    </IButton>
  </div>
</template>
