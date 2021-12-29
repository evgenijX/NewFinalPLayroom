<template>
  <v-app>
      <Header style="position: relative; z-index: 999;"/>
      <router-view />
  </v-app>
</template>

<script>
import Header from "@/components/Home/Header";
export default {
  name: "App",
  components: { Header },
  data: () => ({
    //
  }),
};
</script>
