<template>
  <div>
    <div>마이페이지</div>
  </div>
</template>

<script setup lang="ts">
const userData = false;
if (!userData) {
  throw createError({
    statusCode: 404,
    statusMessage: 'UserData not found'
  });
}
</script>
