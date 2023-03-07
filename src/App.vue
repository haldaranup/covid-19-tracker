<template>
  <Header />
  <router-view />
</template>

<script>
import Header from "./components/Header.vue";

export default {
  components: {
    // eslint-disable-next-line vue/no-unused-components
    Header,
  },
};
</script>
