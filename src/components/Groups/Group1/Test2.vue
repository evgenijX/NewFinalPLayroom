<template>
  <div class="test2">
    <v-parallax
      dark
      src="../../../assets/Groups_age/Group1/paralax_bg.png"
    >
      <div class="about_us">
        <div class="about_us__content-title title-mobile" style="display: none">Комплексне заняття</div>
        <div class="img"><img src="@/assets/Home/img/about_us.png" alt=""></div>
        <div class="about_us__content">
          <div class="about_us__content-title">Комплексне заняття</div>
          <div class="about_us__content-text">
            Для дітей у віці 2-3 років найважливішим є сенсорний розвиток і розвиток дрібної та крупної
            моторики. Все це впливає на формування рецепторів, що відповідають за мову та інтелектуальний
            розвиток.
          </div>
          <div class="about_us__content-text text-two">
            Наші комплексні заняття поділені на 2 частини:
            Перший блок – це заняття з основами математики, де діти вивчають основні величини: кольори,
            форми і розміри, навчаються рахувати цікаві предмети та орієнтуватися в просторі.
            Другий блок – це заняття з основами розвитку мовлення де дітки розвивають мовні навички через
            логоритмічні пісні, імітацію звуків та роботу з картинками.
          </div>
        </div>
      </div>
    </v-parallax>
  </div>

</template>

<script>
export default {
  name: "Test2"
};
</script>

<style scoped>
.test2{
  background-color: #D9F6FF;
}
.sky{
  width: 100%;
  height:
}
.about_us {
  display: flex;
  flex-direction: row-reverse;
  padding: 0 5%;
  justify-content: space-around;
  align-items: center;
  margin-top: 50px;

}

.img img {
  width: 600px;
  margin-right: 20px;
}

.about_us__content-title {
  font-weight: 800;
  font-size: 40px;
  color: #7AD4CB;
}

.about_us__content-text {
  font-weight: 400;
  font-size: 18px;
  color: #7B885C;
  max-width: 700px;
}

.text-two {
  margin-top: 30px;
}

@media screen and (max-width: 1024px) {
  .about_us {
    flex-wrap: wrap;
    flex-direction: column;
  }

  .about_us__content {
    text-align: center;
  }

  .about_us__content-title {
    display: none;
  }

  .title-mobile {
    display: block !important;
  }
}

@media screen and (max-width: 655px) {
  .img img {
    margin: 0;
    max-width: 300px;
  }
}

@media screen and (max-width: 320px) {
  .about_us {
    padding: 0 1%;
  }
}
</style>