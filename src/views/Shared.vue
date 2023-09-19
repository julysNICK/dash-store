<template>
  <div>
    <Overview_shared />
    <List_Users_Shared />
  </div>
</template>

<script setup lang="ts">
import List_Users_Shared from '@/components/List_Users_Shared.vue';


import Overview_shared from '@/components/Overview_shared.vue';



defineProps({
  titlePage: String,
});

</script>

<style scoped></style>