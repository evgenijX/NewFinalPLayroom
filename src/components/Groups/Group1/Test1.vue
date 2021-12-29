<template>
  <div class="about_us">
    <div class="about_us__content-title title-mobile" style="display: none">Особливість віку</div>
    <div class="img"><img src="@/assets/Home/img/about_us.png" alt=""></div>
    <div class="about_us__content">
      <div class="about_us__content-title">Особливість віку</div>
      <div class="about_us__content-text">
        В наймолодшому віці дітям важливо, щоб атмосфера в садочку була як дома. Вони звикають бути без мами і основною задачею педагогів стає їх соціалізація, адаптація та, безумовно, гармонійний розвиток.
        Збалансовані заняття проходять протягом дня, чергуються з прогулянками, іграми та 5-разовим харчуванням. Все відбувається в ритмі дитини з індивідуальним підходом.
      </div>
      <div class="about_us__content-text text-two">
        Діти можуть перебувати в садочку з 8:00 до 19:00.
        В групі знаходяться до 15 дітей з ними 3 педагоги і няня.
        Також до малюків приходять педагоги на англійську мову, тренер в басейн, функціональне
        тренування, творчі заняття та музику.
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Test1"
};
</script>

<style scoped>
.about_us {
  display: flex;
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