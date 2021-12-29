<template>
  <v-app>
    <Landing />
    <About_us />
    <Timetable />
    <Our_benefits />
    <Why_us />
    <Contact />
  </v-app>
</template>

<script>


import Landing from "@/components/Home/Landing";
import About_us from "@/components/Home/About_us";
import Timetable from "@/components/Home/Timetable";
import Our_benefits from "@/components/Home/Our_benefits";
import Why_us from "@/components/Home/Why_us";
import Contact from "@/components/Home/Contact";
export default {
  name: "Home",

  components: {
    Contact,
    Why_us,
    Our_benefits,
    Timetable,
    About_us,
    Landing,

  },
};
</script>
