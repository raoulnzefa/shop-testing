<template>
  <div class="flex space-x-4" v-for="link in links" :key="link.text">
    <a
      :href="link.url"
      class="px-3 py-2 text-sm font-medium text-gray-300 rounded-md hover:bg-gray-700 hover:text-white"
      >{{ link.text }}</a
    >
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      links: [
        {
          url: "#",
          text: "Espace personnel",
        },
        {
          url: "#",
          text: "Commandes",
        },
        {
          url: "#",
          text: "Réductions",
        },
      ],
    };
  },
};
</script>