<template>
  <div>
    <Overview_Content :title="titlePage" />
  </div>
</template>

<script setup lang="ts">

import Overview_Content from '@/components/Overview_Content.vue';


defineProps({
  titlePage: String,
});

</script>

<style scoped></style>