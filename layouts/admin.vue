<template>
  <div>
    <header>
      <div class="navbar">
        <div class="navbar-action">
          <NuxtLink v-slot="{ navigate }" to="/">
            <button @click="navigate()">홈페이지</button>
          </NuxtLink>
          <NuxtLink v-slot="{ navigate }" to="/admin">
            <button @click="navigate()">Admin</button>
          </NuxtLink>
          <NuxtLink v-slot="{ navigate }" to="/login">
            <button @click="navigate()">Login</button>
          </NuxtLink>
        </div>
      </div>
    </header>
    <main>
      <slot></slot>
    </main>
    <footer>
      <div>푸터</div>
    </footer>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
body {
  margin: 0;
  font-family: Arial, sans-serif;
}

header {
  background-color: #007bff;
  border-bottom: 1px solid #007bff;
  padding: 10px 20px;
}

.navBar {
  display: flex;
}
.navbar-action {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  gap: 10px;
}

.navbar-action button {
  background-color: #fff;
  color: black;
  border: none;
  padding: 8px 15px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.navbar-action button:hover {
  background-color: #1c1c1d;
}
</style>
