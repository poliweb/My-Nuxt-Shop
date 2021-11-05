<template>
  <div>
    <header class="text-gray-600 body-font">
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
</style>
