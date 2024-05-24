<template>
  <div>
    <AuthPageTitle title="SignUp" />
    <AuthPageDescription description="Nuxt 연습" />
    <form @submit.prevent="signUpSubmit">
      <input v-model="signUpForm.id" />
      <input v-model="signUpForm.name" />
      <input v-model="signUpForm.password" />
      <input v-model="signUpForm.passwordCheck" />
      <div>
        <button type="submit">로그인</button>
      </div>
    </form>
  </div>
</template>

<script setup lang="ts">
definePageMeta({
  layout: 'false'
});
const signUpForm = ref({
  id: '',
  name: '',
  password: '',
  passwordCheck: ''
});

const signUpSubmit = () => {
  return 0;
};
</script>
