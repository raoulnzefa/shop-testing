<template>
  <nav class="bg-gray-900">
    <div class="mx-auto max-w-7xl sm:px-6 lg:px-8">
      <div class="relative flex items-center justify-between h-16">
        <div
          class="absolute inset-y-0 left-0 flex items-center sm:hidden"
        ></div>
        <div
          class="flex items-center justify-center flex-1 sm:items-stretch sm:justify-start"
        >
          <div class="flex items-center flex-shrink-0">
            <HomeSvg
              classes="block w-auto h-8 text-white fill-current lg:hidden"
            />
            <HomeSvg
              classes="hidden w-auto h-8 text-white fill-current lg:block"
            />
          </div>
          <div class="hidden sm:block sm:ml-6">
            <div class="flex space-x-4">
              <a
                href="#"
                class="px-3 py-2 text-sm font-medium text-gray-300 rounded-md hover:bg-gray-700 hover:text-white"
                >Espace personnel</a
              >
              <a
                href="#"
                class="px-3 py-2 text-sm font-medium text-gray-300 rounded-md hover:bg-gray-700 hover:text-white"
                >Commandes</a
              >
              <a
                href="#"
                class="px-3 py-2 text-sm font-medium text-gray-300 rounded-md hover:bg-gray-700 hover:text-white"
                >Réductions</a
              >
            </div>
          </div>
        </div>
        <div
          class="absolute inset-y-0 right-0 flex items-center pr-2 sm:static sm:inset-auto sm:ml-6 sm:pr-0"
        >
          <!-- Notification Menu -->
          <div class="relative ml-3">
            <button
              class="flex p-1 text-gray-400 bg-gray-800 rounded-full hover:text-white focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-offset-gray-800 focus:ring-white"
              id="notification-menu"
              aria-haspopup="true"
              @click.prevent="(isNotif = !isNotif), (isOpen = false)"
            >
              <span class="sr-only">View notifications</span>
              <svg
                class="w-6 h-6"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
                aria-hidden="true"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9"
                />
              </svg>
            </button>
            <div
              class="absolute right-0 py-1 mt-2 origin-top-right bg-white border border-gray-300 rounded-lg shadow-lg w-max"
              aria-orientation="vertical"
              aria-labelledby="notification-menu"
              v-show="isNotif"
            >
              <div class="px-2">
                <svg
                  width="24"
                  height="24"
                  viewBox="0 0 1792 1792"
                  fill="#44C997"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M1299 813l-422 422q-19 19-45 19t-45-19l-294-294q-19-19-19-45t19-45l102-102q19-19 45-19t45 19l147 147 275-275q19-19 45-19t45 19l102 102q19 19 19 45t-19 45zm141 83q0-148-73-273t-198-198-273-73-273 73-198 198-73 273 73 273 198 198 273 73 273-73 198-198 73-273zm224 0q0 209-103 385.5t-279.5 279.5-385.5 103-385.5-103-279.5-279.5-103-385.5 103-385.5 279.5-279.5 385.5-103 385.5 103 279.5 279.5 103 385.5z"
                  />
                </svg>
              </div>
              <div class="ml-2 mr-6 text-sm">
                <span class="font-semibold">Commande #X100 enregistrée !</span>
                <span class="block text-gray-500"
                  >Rendez-vous sur votre espace personnel</span
                >
              </div>
            </div>
          </div>
          <!-- User Menu -->
          <div class="relative ml-3">
            <button
              class="flex text-sm bg-gray-800 rounded-full focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-offset-gray-800 focus:ring-white"
              id="user-menu"
              aria-haspopup="true"
              @click.prevent="(isOpen = !isOpen), (isNotif = false)"
            >
              <span class="sr-only">Open user menu</span>
              <svg
                class="w-8 h-8 text-white rounded-full fill-current"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 20 20"
                fill="currentColor"
              >
                <path
                  fill-rule="evenodd"
                  d="M10 9a3 3 0 100-6 3 3 0 000 6zm-7 9a7 7 0 1114 0H3z"
                  clip-rule="evenodd"
                />
              </svg>
            </button>
            <div
              class="absolute right-0 w-48 py-1 mt-2 origin-top-right bg-white rounded-md shadow-lg ring-1 ring-black ring-opacity-5"
              role="menu"
              aria-orientation="vertical"
              aria-labelledby="user-menu"
              v-show="isOpen"
            >
              <a
                href="#"
                class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100"
                role="menuitem"
                >Profil</a
              >
              <a
                href="#"
                class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100"
                role="menuitem"
                >Paramètres</a
              >
              <a
                href="#"
                class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100"
                role="menuitem"
                >Déconnexion</a
              >
            </div>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>

<script setup>
import HomeSvg from "./HomeSvg.vue";
</script>

<script>
export default {
  data: function () {
    return {
      isOpen: false,
      isNotif: false,
    };
  },
  methods: {
    close(e) {
      if (!this.$el.contains(e.target)) {
        this.isOpen = false;
        this.isNotif = false;
      }
    },
  },
  mounted() {
    document.addEventListener("click", this.close);
  },
  beforeDestroy() {
    document.removeEventListener("click", this.close);
  },
};
</script>