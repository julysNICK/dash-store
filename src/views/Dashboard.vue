<template>
  <div>
    <Overview :title="titlePage" />
    <Activity />
  </div>
</template>

<script setup lang="ts">
import Activity from '@/components/Activity.vue';
import Overview from '@/components/Overview.vue';


defineProps({
  titlePage: String,
});

</script>

<style scoped></style>