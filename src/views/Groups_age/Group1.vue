<template>
<v-app>
  <Landing />
  <Test1 />
  <Test2 />
  <Test1 />
  <Test2 />
  <Contact/>
</v-app>
</template>

<script>
import Landing from "@/components/Groups/Group1/Landing";
import Test1 from "@/components/Groups/Group1/Test1";
import Test2 from "@/components/Groups/Group1/Test2";
import Contact from "@/components/Home/Contact";
export default {
  name: "Group2-3",
  components: { Contact, Test2, Test1, Landing }
};
</script>

<style scoped>

</style>