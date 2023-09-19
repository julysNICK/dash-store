<script setup lang="ts">

</script>

<template>
  <div class="activity">
    <div class="title">
      <i class="uil uil-clock"></i>
      <span class="text">
        Users Likes
      </span>
    </div>

    <div class="activity-data">
      <div class="data names">

        <span class="data-title">
          Name
        </span>
        <span class="data-list">
          Prem Sahi
        </span>
        <span class="data-list">
          Prem Sahi
        </span>
        <span class="data-list">
          Prem Sahi
        </span>

      </div>
      <div class="data email">
        <span class="data-title">
          Email
        </span>
        <span class="data-list">
          julysTest@gmail.com
        </span>
        <span class="data-list">
          julysTest@gmail.com
        </span>
        <span class="data-list">
          julysTest@gmail.com
        </span>
      </div>
      <div class="data joined">
        <span class="data-title">
          Joined
        </span>
        <span class="data-list">
          2023-01-01
        </span>
        <span class="data-list">
          2023-01-01
        </span>
        <span class="data-list">
          2023-01-01
        </span>
      </div>
      <div class="data status">
        <span class="data-title">
          Status
        </span>
        <span class="data-list">
          Liked
        </span>
        <span class="data-list">
          Liked
        </span>
        <span class="data-list">
          Liked
        </span>
      </div>
    </div>

  </div>
</template>

<style scoped>
.title {
  display: flex;
  align-items: center;
  margin: 60px 0 30px 0;
}

.title .text {
  font-size: 24px;
  font-weight: 500;
  margin-left: 5px;
  color: var(--text-color);
}

.title i {
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

.activity .activity-data {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  flex-direction: row;
}

.activity .activity-data {
  display: flex;

}

.activity-data .data {
  display: flex;
  flex-direction: column;
  margin: 0 15px;
}

.activity-data .data-title {
  font-size: 20px;
  font-weight: 500;
  color: var(--text-color);
}

.activity-data .data .data-list {
  font-size: 18px;
  font-weight: 400;
  color: var(--text-color);
  margin-top: 20px;
  white-space: nowrap;
}

@media (max-width:1000px) {

  .activity .activity-data {
    overflow-y: scroll;
  }

}
</style>