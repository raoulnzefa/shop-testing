<template>
  <a :href="href" :class="classe" :role="role"><slot /></a>
</template>

<script>
export default {
  props: {
    classe: {
      type: String,
      default: "classes",
    },
    href: {
      type: String,
      default: "#",
    },
    role: {
      type: String,
      default: "none",
    },
  },
};
</script>