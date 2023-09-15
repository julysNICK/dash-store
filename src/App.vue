<script setup lang="ts">
import NavbarDash from './components/NavbarDash.vue';
import NavbarTop from './components/NavbarTop.vue';




</script>

<template>
  <NavbarDash />
  <section class="dashboard">
    <NavbarTop />

    <div class="dashboard-content">
      <div class="overview">
        <div class="title">
          <i class="uil uil-tachometer-fast"></i>
          <span class="text">
            Dashboard
          </span>
        </div>
        <div class="boxes">
          <div class="box box1">
            <i class="uil uil-thumbs-up"></i>
            <span class="text">
              Total Likes
            </span>
            <span class="number">
              50,120
            </span>
          </div>
          <div class="box box2">
            <i class="uil uil-comment-alt"></i>
            <span class="text">
              Total Comments
            </span>
            <span class="number">
              50,120
            </span>
          </div>
          <div class="box box3">
            <i class="uil uil-share"></i>
            <span class="text">
              Total Share
            </span>
            <span class="number">
              50,120
            </span>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<style scoped>
@import url('https://unicons.iconscout.com/release/v4.0.8/css/line.css');

@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@200;300;400;500;600&display=swap');

* {
  font-family: 'Poppins', sans-serif;
}

.dashboard {
  position: relative;
  left: 250px;
  background-color: var(--panel-color);
  height: 100vh;
  width: calc(100% - 250px);
  padding: 10px 14px;
  transition: var(--tran-05);
}


nav.close~.dashboard {
  left: 73px;
  width: calc(100% - 73px);
}

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
  color: var(--title-color);
}

.dashboard-content .boxes {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.dashboard-content .boxes .box {
  display: flex;
  flex-direction: column;
  align-items: center;
  border-radius: 10px;
  width: calc(100% / 3 - 15px);
  padding: 15px 20px;
  background-color: var(--box1-color);
}
</style>
