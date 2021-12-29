<template>
  <div class="header_top">
    <Header_language />
    <Header_location />
    <div class="social_icons" style="display: flex;column-gap: 20px">
      <a href="https://www.instagram.com/playroom.kyiv/?utm_medium=copy_link"><img src="@/assets/Header/inst.svg" alt=""></a>
      <a href="https://www.facebook.com/playroom.co.ua/"><img src="@/assets/Header/fb.svg" alt=""></a>
    </div>
  </div>
</template>

<script>

import Header_language from "@/components/Home/Header_component/Header_language";
import Header_location from "@/components/Home/Header_component/Header_location";
export default {
  name: "Header_top",
  components: { Header_location, Header_language },
}
</script>

<style scoped>
.header_top{
  padding: 10px 10%;
  display: flex;
  justify-content: space-between;
  background-image: url("../../../assets/Header/bg_header-top.png");
  background-size: cover;
  background-repeat: no-repeat;
  align-items: center;
}

</style>