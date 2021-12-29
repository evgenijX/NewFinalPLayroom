<template>
<v-app>
  <Landing />
  <Test1 />
  <Test2 />
  <Test1 />
  <Test2 />
</v-app>
</template>

<script>
import Landing from "@/components/Groups/Group1/Landing";
import Test1 from "@/components/Groups/Group1/Test1";
import Test2 from "@/components/Groups/Group1/Test2";
export default {
  name: "Group2-3",
  components: { Test2, Test1, Landing }
};
</script>

<style scoped>

</style>