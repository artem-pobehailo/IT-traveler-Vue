<script setup>
import { reactive, toRaw, watch } from 'vue'
import FormContainer from '../FormContainer.vue'
import IInput from '@/components/IInput/IInput.vue'
import IButton from '@/components/IButton/IButton.vue'

const emit = defineEmits(['submit'])
const userData = reactive({
  email: '',
  password: '',
})

watch(
  userData,
  () => {
    console.log('user data changed')
  },
  { immediate: true },
)
</script>

<template>
  <FormContainer
    @submit.prevent="emit('submit', toRaw(userData))"
    class="max-w-[500px] w-full bg-white p-10 rounded-r-2xl"
  >
    <IInput
      class="mb-4"
      label="Електронна пошта"
      placeholder="email@gmail.com"
      v-model="userData.email"
    />
    <IInput label="Пароль" type="password" v-model="userData.password" />
    <IButton class="mt-10 w-full" variant="gradient" type="submit">Увійти </IButton>
  </FormContainer>
</template>
