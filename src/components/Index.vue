<template>
  <div><AppHeader /> <AppSection /> <AppFooter /></div>
</template>

<script>
import AppHeader from "./AppHeader.vue";
import AppSection from "./AppSection.vue";
import AppFooter from "./AppFooter.vue";

export default {
  name: "Index",
  components: {
    AppHeader,
    AppSection,
    AppFooter
  }
};
</script>
