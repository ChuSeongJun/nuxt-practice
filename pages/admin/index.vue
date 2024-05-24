<template>
  <section>
    <div>관리자 페이지</div>
    <div>관리자 페이지입니다다다</div>
  </section>
</template>

<script setup lang="ts">
definePageMeta({
  layout: 'admin'
});

const add = <T extends number | string>(x: T, y: T): T => {
  return x + y;
};

const toArray = <T>(a: T, b: T): T[] => {
  return [a, b];
};
</script>

<style scoped></style>
