<template>
  <div class="landing">
    <div class="landing__main_content">
      <h1 class="landing__main_content-title">Вік 2-3 роки</h1>
    </div>
  </div>
</template>

<script>
export default {
  name: "Landing"
};
</script>

<style scoped>
.landing__main_content{
  background-image: url("../../../assets/Groups_age/Group1/Main_bg.gif");
  background-size: cover;
  background-repeat: no-repeat;
  height: 500px;
  width: 100vw;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}
.landing__main_content-title{
  font-size: 50px;
  color: #357364;
}

</style>