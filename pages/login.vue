<template>
  <div class="loginSection">
    <AuthPageTitle title="Login" />
    <AuthPageDescription description="Nuxt 연습" />
    <form class="loginForm" @submit.prevent="loginSubmit">
      <input v-model="loginForm.id" placeholder="Email" />
      <input v-model="loginForm.password" placeholder="Password" type="password" />
      <div>
        <button type="submit">로그인</button>
      </div>
      <div>
        <div>아직 회원이 아니신가요?</div>
        <NuxtLink v-slot="{ navigate }" to="signup">
          <button @click="navigate()">회원가입</button>
        </NuxtLink>
      </div>
    </form>
  </div>
</template>

<script setup lang="ts">
definePageMeta({
  layout: 'false'
});
const loginForm = ref({
  id: '',
  password: ''
});

const loginSubmit = () => {
  return 0;
};
</script>

<style scoped>
.loginSection {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background-color: #f8f8f8;
}

.loginForm {
  width: 400px;
  background: #fff;
  padding: 40px 30px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  border-radius: 8px;
}

.loginForm input {
  width: 100%;
  padding: 12px 15px;
  margin-bottom: 20px;
  border: 1px solid #ddd;
  border-radius: 5px;
  font-size: 14px;
  box-sizing: border-box;
}

.loginForm input:focus {
  border-color: #7d4cdb;
  outline: none;
}

.loginForm button[type='submit'] {
  width: 100%;
  padding: 12px 15px;
  background-color: #7d4cdb;
  border: none;
  border-radius: 5px;
  color: white;
  font-size: 16px;
  cursor: pointer;
  transition: background-color 0.3s;
}

.loginForm button[type='submit']:hover {
  background-color: #5c32b6;
}

.loginForm div {
  margin-top: 10px;
  text-align: center;
  font-size: 14px;
}

.loginForm div a {
  color: #7d4cdb;
  text-decoration: none;
}

.loginForm div a:hover {
  text-decoration: underline;
}
</style>
