<script setup lang="ts">
import CardBox from './CardBox.vue';

</script>

<template>
  <div class="overview">
    <div class="title">
      <!-- <i class="uil uil-tachometer-fast"></i> -->
      <span class="text">
        Likes Page
      </span>
    </div>


  </div>
</template>

<style scoped>
.dashboard .dashboard-content {
  padding-top: 50px;
}

.dashboard-content .title {
  display: flex;
  align-items: center;
  margin: 60px 0 30px 0;
}

.dashboard-content .title i {
  position: relative;
  height: 35px;
  width: 35px;
  background-color: var(--primary-color);
  border-radius: 50%;
  color: var(--title-icon-color);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 24px;
}

.dashboard-content .title .text {
  font-size: 24px;
  font-weight: 500;
  margin-left: 10px;
  color: var(--text-color);
}
</style>