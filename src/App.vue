<script setup lang="ts">
import NavbarDash from './components/NavbarDash.vue';
import NavbarTop from './components/NavbarTop.vue';
import Overview from './components/Overview.vue';




</script>

<template>
  <NavbarDash />
  <section class="dashboard">
    <NavbarTop />

    <div class="dashboard-content">
      <Overview />

      <div class="activity">
        <div class="title">
          <i class="uil uil-clock"></i>
          <span class="text">
            Recent Activity
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

/* Activity */
.dashboard-content .activity .activity-data {
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



  nav~.dashboard .top {
    left: 73px;
    width: calc(100% - 73px);
  }

  nav~.dashboard {
    left: 73px;
    width: calc(100% - 73px);

  }

  nav.close~.dashboard {
    left: 250px;
    width: calc(100% - 250px);
  }

}
</style>
