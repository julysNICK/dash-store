<script setup lang="ts">
// import { RouterLink, RouterView } from 'vue-router'
// import HelloWorld from './components/HelloWorld.vue'

import { onMounted } from "vue";


const methodsClick = {
  onloadBody() {

    const body = document.querySelector("body");
    const mode = localStorage.getItem("mode");

    if (mode === "dark") {
      body && body.classList.add("dark");
    } else {
      body && body.classList.remove("dark");
    }
  },



  toggleMode() {
    console.log("chamei");
    const body = document.querySelector("body");
    body && body.classList.toggle("dark");

    if (body && body.classList.contains("dark")) {
      localStorage.setItem("mode", "dark");
    } else {
      localStorage.setItem("mode", "light");
    }
  },
};

onMounted(() => {

  methodsClick.onloadBody();
});




</script>

<template>
  <nav>
    <div class="logo-name">
      <div class="logo-image">
        <img src="https://api.freelogodesign.org/assets/thumb/logo/a17b07eb64d341ffb1e09392aa3a1698_400.png" alt="logo" />
      </div>
      <span class="logo_name"> Julys </span>
    </div>
    <div class="menu-items">
      <ul class="nav-links">
        <li>
          <a href="#">
            <i class="uil uil-home"></i>
            <span class="link-name"> Dashboard </span>
          </a>
        </li>
        <li>
          <a href="#">
            <i class="uil uil-analytics"></i>
            <span class="link-name"> Content </span>
          </a>
        </li>
        <li>
          <a href="#">
            <i class="uil uil-link"></i>
            <span class="link-name"> Like </span>
          </a>
        </li>
        <li>
          <a href="#">
            <i class="uil uil-comment-alt-dots"></i>
            <span class="link-name"> Comment </span>
          </a>
        </li>
        <li>
          <a href="#">
            <i class="uil uil-share"></i>
            <span class="link-name"> Share </span>
          </a>
        </li>
      </ul>

      <ul class="logout-mode">
        <li>
          <a href="#">
            <i class="uil uil-sign-out-alt"></i>
            <span class="link-name"> Logout </span>
          </a>
        </li>
        <li class="mode">
          <a href="#">
            <i class="uil uil-moon"></i>
            <span class="link-name"> Dark Mode </span>
          </a>

          <div class="mode-toggle" @click="methodsClick.toggleMode">
            <span class="switch"> </span>
          </div>
        </li>
      </ul>
    </div>
  </nav>
</template>

<style scoped>
@import url("https://unicons.iconscout.com/release/v4.0.8/css/line.css");

@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@200;300;400;500;600&display=swap");

nav {
  position: fixed;
  top: 0;
  left: 0;
  height: 100%;
  width: 250px;
  padding: 10px 14px;
  background-color: var(--panel-color);
  border-right: 1px solid var(--border-color);
  transition: var(--tran-03);
}

nav.close {
  width: 73px;
}

nav .logo-image {
  display: flex;
  justify-content: center;
  justify-content: center;
  min-width: 45px;
}

nav .logo-image img {
  width: 40px;
  object-fit: cover;
  border-radius: 50%;
}

nav .logo-name {
  display: flex;
  align-items: center;
}

nav .logo-name .logo_name {
  font-size: 1.5rem;
  font-weight: 600;
  color: var(--text-color);
  margin-left: 10px;
  transition: var(--tran-05);
}

nav.close .logo_name {
  opacity: 0;
  pointer-events: none;
}

nav .menu-items {
  margin-top: 20px;
  height: calc(100% - 90px);
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.menu-items li {
  list-style: none;
}

.menu-items li a {
  display: flex;
  align-items: center;
  height: 50px;
  text-decoration: none;
  position: relative;
}

.nav-links li a:hover:before {
  content: "";
  position: absolute;
  height: 5px;
  width: 5px;
  border-radius: 50%;
  background-color: var(--primary-color);
  left: -7px;
}

body.dark li a:hover:before {
  background-color: var(--text-color);
}

.menu-items li a i {
  font-size: 24px;
  min-width: 45px;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--black-light-color);
}

.menu-items li a .link-name {
  font-size: 18px;
  font-weight: 400;
  color: var(--black-light-color);
  transition: var(--tran-05);
}

nav.close li a .link-name {
  opacity: 0;
  pointer-events: none;
}

.nav-links li a:hover i,
.nav-links li a:hover .link-name {
  color: var(--primary-color);
}

body.dark .nav-links li a:hover i,
body.dark .nav-links li a:hover .link-name {
  color: var(--text-color);
}

.menu-items .logout-mode {
  padding-top: 20px;
  border-top: 1px solid var(--border-color);
}

.menu-items .mode {
  display: flex;
  align-items: center;
  white-space: nowrap;
}

.menu-items .mode-toggle {
  position: absolute;
  right: 14px;
  height: 50px;
  min-width: 45px;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
}

.mode-toggle .switch {
  display: inline-block;
  position: relative;
  height: 22px;
  width: 40px;
  background-color: var(--toggle-color);
  border-radius: 30px;
}

.switch:before {
  content: "";
  position: absolute;
  height: 15px;
  width: 15px;
  border-radius: 50%;
  background-color: var(--panel-color);
  top: 50%;
  left: 5px;
  transition: var(--tran-03);
  transform: translateY(-50%);
}

body.dark .switch:before {
  left: calc(100% - 20px);
}

@media (max-width: 1000px) {
  nav {
    width: 73px;
  }

  nav .logo_name {
    opacity: 0;
    pointer-events: none;
  }

  nav.close {
    width: 250px;
  }

  nav li a .link-name {
    opacity: 0;
    pointer-events: none;
  }

  nav.close li a .link-name {
    opacity: 1;
    pointer-events: auto;
  }

  nav.close .logo_name {
    opacity: 1;
    pointer-events: auto;
  }

  nav~.dashboard {
    left: 73px;
    width: calc(100% - 73px);
  }

  nav.close~.dashboard {
    left: 250px;
    width: calc(100% - 250px);
  }

  nav~.dashboard .top {
    left: 73px;
    width: calc(100% - 73px);
  }

  nav.close~.dashboard .top {
    left: 250px;
    width: calc(100% - 250px);
  }

  @media (max-width: 500px) {
    nav {
      width: 73px;
    }

    nav.close {
      width: 73px;
    }

    nav .logo-name {
      opacity: 1;
      pointer-events: none;
    }

    nav.close .logo_name {
      opacity: 0;
      pointer-events: none;
    }

    nav li a .link-name {
      opacity: 0;
    }

    nav.close li a .link-name {
      opacity: 0;
      pointer-events: none;
    }
  }
}
</style>
