<template>
  <div><AppHeader /> <AppFooter /></div>
</template>

<script>
import AppHeader from "./AppHeader.vue";
import AppFooter from "./AppFooter.vue";

export default {
  name: "Index",
  components: {
    AppHeader,
    AppFooter
  }
};
</script>
