<script setup lang="ts">
import NavbarTop from '@/components/NavbarTop.vue';
import Dashboard from './Dashboard.vue';
import NavbarDash from '@/components/NavbarDash.vue';
import { ref } from 'vue';

const namePage = ref('dashboard');


const updateComponentName = (newValue: any) => {
  namePage.value = newValue;
};

</script>

<template>
  <NavbarDash :component_name="namePage" @updateComponentName="updateComponentName" />
  <section class="dashboard">
    <NavbarTop />

    <div class="dashboard-content">

      <Dashboard v-if="namePage === 'dashboard'" titlePage="Dashboard" />


      <Dashboard v-else-if="namePage === 'content'" titlePage="Content" />



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




@media (max-width:500px) {
  nav~.dashboard {
    left: 73px;
    width: calc(100% - 73px);
  }

  nav.close~.dashboard {
    left: 73px;
    width: calc(100% - 73px);
  }

  nav~.dashboard .top {
    left: 73px;
    width: calc(100% - 73px);
  }

  nav.close~.dashboard .top {
    left: 73px;
    width: calc(100% - 73px);
  }


}
</style>
