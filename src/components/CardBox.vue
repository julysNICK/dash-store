<script setup lang="ts">

defineProps({
  title: String,
  icon: String,
  // number: String,
  color: String
})


</script>

<template>
  <div class="box" :class="color">
    <i class="uil" :class="icon"></i>
    <span class="text">
      {{ title }}
    </span>
    <span class="number">
      50,120
    </span>
  </div>
</template>

<style scoped>
.dashboard-content .boxes .box {
  display: flex;
  flex-direction: column;
  align-items: center;
  border-radius: 10px;
  width: calc(100% / 3 - 15px);
  padding: 15px 20px;
  background-color: var(--box1-color);
  flex-wrap: wrap;
}

.boxes .box i {
  font-size: 35px;
  color: var(--text-color)
}

.boxes .box .text {
  white-space: nowrap;
  font-size: 18px;
  font-weight: 500;
  color: var(--text-color);
  margin-top: 10px;
}

.boxes .box .number {
  white-space: nowrap;
  font-size: 40px;
  font-weight: 500;
  color: var(--text-color);
  margin-top: 10px;
}

.boxes .box.box2 {
  background-color: var(--box2-color);
}

.boxes .box.box3 {
  background-color: var(--box3-color);
}

@media (max-width: 780px) {
  .dashboard-content .boxes .box {
    width: calc(100% / 2 - 15px);
    margin-top: 15px;
  }

  .boxes .box .text {
    font-size: 12px;
  }

  .boxes .box .number {
    font-size: 20px;
  }


}

@media (max-width:560px) {
  .dashboard-content .boxes .box {
    width: 100%;

  }

}
</style>