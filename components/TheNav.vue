<template>
  <div>
    <header class="main-tool-bar text-gray-600 body-font relative">
      <div class="container mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center">
        <NuxtLink to="/" class="flex title-font font-medium items-center text-gray-900 mb-4 md:mb-0">
          <Logo/>
          <span class="ml-3 text-xl">PW Shop</span>
        </NuxtLink>
        <nav class="md:ml-auto md:mr-auto flex flex-wrap items-center text-base justify-center">
          <NuxtLink
            v-for="menuLink in menuLinks"
            :key="menuLink.index"
            :to="menuLink.to"
            class="mr-5 hover:text-gray-900"
          >{{ menuLink.title }}</NuxtLink>
        </nav>
        <button
          class="inline-flex items-center bg-gray-100 border-0 py-1 px-3 focus:outline-none hover:bg-gray-200 rounded text-base mt-4 md:mt-0"
        >
          Корзина
          <Cart />
        </button>
      </div>
      <div class="nav-masck absolute w-full h-full top-0 bottom-0 left-0 backdrop-filter backdrop-blur"></div>
    </header>
  </div>
</template>

<script>
import Cart from "./icons/cart.vue";
import Logo from "./icons/Logo.vue";
export default {
  components: {
    Cart,
    Logo,
  },
  data: function () {
    return {
      menuLinks: [
        {
          title: "Главная",
          to: "/",
        },
        {
          title: "Каталог",
          to: "#",
        },
        {
          title: "Блог",
          to: "#",
        },
        {
          title: "Контакты",
          to: "#",
        },
      ],
    };
  },
};
</script>

<style>
.bg-coral {
  background-color: coral;
}
.main-tool-bar {
}
.main-tool-bar.main-tool-bar--scrolled {
  top: 0;
  left: 0;
  width: 100%;
  z-index: 99;
  position: fixed;
  -webkit-animation: fadeInDown 0.5s ease-in-out;
  animation: fadeInDown 0.5s ease-in-out;
  box-shadow: 0 1px 5px 0 rgb(0 0 0 / 20%);
  /* background-color: rgba(255, 255, 255, 0.5); */
}

.main-tool-bar--scrolled .container {
  padding-top: 0.25rem;
  padding-bottom: 0.25rem;
}
.nav-masck {
  background-color: rgb(255, 255, 255);
  z-index: -1;
}
.main-tool-bar--scrolled .nav-masck {
  background-color: rgba(255, 255, 255, 0.7);
  z-index: -1;
}
</style>
