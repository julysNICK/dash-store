<script setup lang="ts">
import NavbarDash from './components/NavbarDash.vue';


const methodsToggleMenu = {
  toggleMode() {
    console.log("chamei")

    const sidebar = document.querySelector('nav')
    sidebar && sidebar.classList.toggle('close')
  }
}

</script>

<template>
  <NavbarDash />
  <section class="dashboard">
    <div class="top">
      <i class="uil uil-bars sidebar-toggle" @click="methodsToggleMenu.toggleMode"></i>

      <div class="search-box">
        <i class="uil uil-search"></i>
        <input type="text" placeholder="Search...">

      </div>
      <img src="https://images.pexels.com/photos/771742/pexels-photo-771742.jpeg?auto=compress&cs=tinysrgb&w=300"
        alt="profile">
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

.dashboard .top {
  position: fixed;
  top: 0;
  left: 250px;
  display: flex;
  width: calc(100% - 250px);
  justify-content: space-between;
  align-items: center;
  padding: 10px 14px;
  background-color: var(--panel-color);
  transition: var(--tran-05);

}

.dashboard .top .sidebar-toggle {
  font-size: 26px;
  cursor: pointer;
  color: var(--text-color);
}

nav.close~.dashboard .top {
  left: 73px;
  width: calc(100% - 73px);
}


nav.close~.dashboard {
  left: 73px;
  width: calc(100% - 73px);
}

.dashboard .top .search-box {
  position: relative;
  height: 45px;
  max-width: 600px;
  width: 100%;
  margin: 0 30px;
}

.top .search-box input {
  position: absolute;
  border: 1px solid var(--border-color);
  background-color: var(--panel-color);
  padding: 0 25px 0 50px;
  border-radius: 6px;
  height: 100%;
  width: 100%;
  color: var(--text-color);
  font-size: 15px;
  font-weight: 400;
  outline: none;
}

.top .search-box i {
  position: absolute;
  left: 15px;
  z-index: 1;
  font-size: 22px;
  top: 50%;
  transform: translateY(-50%);
  color: var(--black-light-color);
}

.top img {
  width: 40px;
  border-radius: 50%;
}
</style>
