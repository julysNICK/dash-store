<template>
  <div>
    <Overview_Like />
    <List_users_likes />
  </div>
</template>

<script setup lang="ts">
import List_users_likes from '@/components/List_users_likes.vue';
import Overview_Like from '@/components/Overview_Like.vue';



defineProps({
  titlePage: String,
});

</script>

<style scoped></style>