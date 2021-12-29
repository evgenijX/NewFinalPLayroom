<template>
  <div class="about_us">
    <div class="about_us__content-title title-mobile" style="display: none">Про нас</div>
    <div class="img"><img src="@/assets/Home/img/about_us.png" alt=""></div>
    <div class="about_us__content">
      <div class="about_us__content-title">Про нас</div>
      <div class="about_us__content-text">
        Шукаєте дружнє місце для дітей, де вони могли б навчатися, грати,
        рухатися, творити годинами та ніколи не нудьгувати? І все це – переважно англійською мовою?
      </div>
      <div class="about_us__content-text text-two">
        Playroom – це англомовний садочок, де вивчати англійську мову легко та
        цікаво. Діти спілкуються як з носіями мови, так і українськими вчителями
        з досконалим знанням англійської мови, що створює природні умови для
        кращого засвоєння англійської. Наші викладачі дуже люблять дітей і свою
        роботу. Викладання дітям ведеться англійською мовою. Садок «Playroom» –
        це затишне місце з просторим залом, арт-кімнатою, класом музики,
        яскравими кімнатами для кожної з грум, зонами для ігор і дитячою
        бібліотекою. Діти навчаються через гру.
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "About_us"
};
</script>

<style scoped>
.about_us {
  display: flex;
  padding: 0 5%;
  justify-content: space-around;
  align-items: center;
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