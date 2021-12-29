<template>
  <div class="landing">
    <div class="landing__content">
      <div class="landing__content-title">Playroom</div>
      <div class="landing__content-subtitle">Ваш англомовний садочок з білінгвальним методом навчання</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Landing",
}
</script>

<style scoped>
.landing__content{
  background-image: url("../../assets/Home/bg/bg_landing.svg");
  background-size: cover;
  background-repeat: no-repeat;
  height: 100vh;
  width: 100vw;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}
.landing__content-title{
  font-weight: 800;
  font-size: 80px;
  color: #7AD4CB;
}
.landing__content-subtitle{
  font-size: 45px;
  text-align: center;
  color: #FFFFFF;
  text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  min-width: 310px;
  max-width: 900px;
}
@media screen and (max-width: 320px) {
  .landing__content-title {
    font-size: 60px;
  }
  .landing__content-subtitle{
    font-size: 30px;
  }
}

</style>