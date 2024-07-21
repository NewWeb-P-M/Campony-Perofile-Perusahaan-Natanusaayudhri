<template>
  <div class="pembatasheader">
    <div class="destop">
      <div>
        <nav :class="['nav', { 'navbar-visible': isVisible }]">
          <div class="logo">
            <img src="../assets/img/LogoHead.png" alt="Logo">
          </div>
          <div class="search">
            <ul>
              <li><a href="#">Home</a></li>
              <li><a href="#tentangSaya">Tentang Saya</a></li>
              <li><a href="#konsultasi">Konsultasi</a></li>
              <li><a href="#artikel">Artikel</a></li>
            </ul>
          </div>
        </nav>
        <!-- Konten halaman lainnya -->
      </div>
    </div>
    <!-- drawer init and toggle -->
    <div class="drawerMenu  text-center">
      <div class="logo">
        <img src="../assets/img/LogoHead.png" alt="Logo">
      </div>
      <!-- <button
        class="text-black  focus:ring-4 focus:ring-blue-300 font-medium rounded-lg text-sm dark:bg-blue-600 dark:hover:bg-blue-700 focus:outline-none dark:focus:ring-blue-800"
        type="button" data-drawer-target="dropdownHover" data-drawer-show="dropdownHover" data-drawer-placement="right"
        aria-controls="dropdownHover">
        <svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" fill="currentColor" class="bi bi-list"
          viewBox="0 0 16 16">
          <path fill-rule="evenodd"
            d="M2.5 12a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5m0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5m0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5" />
        </svg>
      </button> -->
      <button id="dropdownHoverButton" data-dropdown-toggle="dropdownHover" data-dropdown-trigger="hover"
        class="text-white focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center inline-flex items-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
        type="button"><svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" fill="currentColor" class="bi bi-list"
          viewBox="0 0 16 16">
          <path fill-rule="evenodd"
            d="M2.5 12a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5m0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5m0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5" />
        </svg>
      </button>

    </div>

    <!-- drawer component -->
    <div id="dropdownHover"
      class="z-10 hidden text-center bg-white divide-y divide-gray-100 rounded-lg shadow w-44 dark:bg-gray-700">
      <ul class="py-2 text-sm text-gray-700 dark:text-gray-200" aria-labelledby="dropdownHoverButton">
        <li>
          <a href="#"
            class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">Home</a>
        </li>
        <li>
          <a href="#tentangSaya"
            class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">Tentang Saya</a>
        </li>
        <li>
          <a href="#konsultasi"
            class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">Konsultasi</a>
        </li>
        <li>
          <a href="#artikel" class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">Artikel</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { ref, onMounted, onUnmounted } from 'vue';

const isVisible = ref(false);

const handleScroll = () => {
  if (window.scrollY > 100) {
    isVisible.value = true;
  } else {
    isVisible.value = false;
  }
};

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
});
</script>

<style scoped>
.drawerMenu {
  display: none;
}

.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-left: 20px;
  padding-right: 20px;
  position: fixed;
  top: 50px;
  left: 0;
  right: 0;
  transition: top 0.5s ease-in-out;
  background-color: white;
  /* Tambahkan background-color jika diperlukan */
  z-index: 1;
  /* Agar navigasi tetap di atas konten lainnya */
}

.navbar-visible {
  top: 0;
}

.logo img {
  width: 130px;
  height: 80px;
}

.search {
  width: 400px;
}

.search ul {
  display: flex;
  justify-content: space-between;
}

.search ul li a {
  font-weight: bold;
  position: relative;
  text-decoration: none;
  color: inherit;
}

.search ul li a:before {
  content: "";
  position: absolute;
  width: 0;
  height: 2px;
  bottom: -3px;
  left: 0;
  background-color: #3687aa;
  visibility: hidden;
  transition: all 0.5s ease-in-out;
}

.search ul li a:hover:before,
.search ul li a:focus:before {
  visibility: visible;
  width: 100%;
}

.search ul li a:hover,
.search ul li a:focus {
  color: #3687aa;
}

.cliksearch {
  padding: 10px;
}

.cliksearch i {
  font-size: 25px;
}

@media (max-width: 600px) {
  .destop {
    display: none;
  }

  .pembatasheader {
    background-color: #3687aa;
    text-align: end;
    display: flex;
    justify-content: end;

  }

  .drawerMenu {
    position: fixed;
    z-index: 100;
    background-color: rgba(0, 0, 0, 0.2);
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    padding-right: 10px;
  }

  .logo img {
    width: 70px;
    padding-left: 10px;
    height: 40px;
  }
}
</style>