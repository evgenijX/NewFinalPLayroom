<template>
  <div class="Our_benefits">
    <div class="top_cloud-bg"></div>
    <div class="Our_benefits__title">Наші переваги</div>
    <div class="test">
      <div class="Our_benefits__content" v-for="item in items" :key="item.title">
        <div class="Our_benefits__content-gif"> <img :src="item.gif"/> </div>
        <div class="Our_benefits__content-title"> {{item.title}} </div>
      </div>
    </div>
    <div class="main__content__text">Наш освітній підхід включає елементи <span>«RESPONSIVE CLASSROOM».</span> Всім відомо, що успішне дитина – це щаслива дитина. Для нас надзвичайно важливо, щоб між учителем і учнем завжди відбувався діалог, щоб вони співпрацювали. Дітям потрібно досягати вершин – адже їхній ключик до успіху – не боятись робити помилки. Помилки – це ще одна із можливостей навчатися.</div>
    <div class="main__content__text second_text">У Сполучених Штатах Америки підхід <span>«RESPONSIVE CLASSROOM»</span> був реалізований в багатьох дошкільних навчальних закладах та виявився надзвичайно ефективним. Він підтверджений багатьма дослідженнями, за його допомогою досягаються підвищення успішності, зменшення  проблем з поведінкою, розвиток соціальних навичок і реалізація більш якісної освіти.</div>
    <div class="bottom_cloud-bg"></div>
  </div>
</template>

<script>
export default {
  name: "Our_benefits",
  data: () => {
    return ({
      model: null,
      items: [
        { title: "Дитина - занурена в англомовне середовище.",gif: require("../../assets/Home/gif/First.gif")},
        { title: "Знаходимо баланс між структурованим навчанням та пізнавальними іграми для ваших діток.", gif: require("../../assets/Home/gif/secondIcon.gif")},
        { title: "Наш пріоритет – це творчий підхід.", gif: require("../../assets/Home/gif/thirdicon.gif")},
        { title: "Кожен вид діяльності спрямований на стимулювання креативного, творчого мислення у дитини.",gif: require("../../assets/Home/gif/fouthicon.gif")},
      ]
    });
  },
}
</script>

<style scoped>
.Our_benefits{
  background-color: #D9F6FF;
  background-image: url("../../assets/Home/bg/bg_cloud.svg");
  background-size: cover;
  background-repeat: no-repeat;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}
.Our_benefits__title{
  font-weight: 800;
  font-size: 40px;
  color: #7AD4CB;
}
.Our_benefits__content{
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 0 10%;
  max-width: 400px;
  text-align: center;
  margin-bottom: 50px;

}
.Our_benefits__content-gif{
  width: 388px;
  height: 388px;
  background: #FFFFFF;
  box-shadow: inset 0px 8px 7px rgba(0, 0, 0, 0.25);
  filter: drop-shadow(0px 4px 23px rgba(70, 143, 159, 0.78));
  border-radius: 50%;
  margin-bottom: 15px;
}
.Our_benefits__content-gif img{
  max-width: 380px;
  border-radius: 50%;
}
.test{
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
.Our_benefits__content-title{
  font-size: 20px;
  line-height: 24px;
  color: #357364;
}
.top_cloud-bg{
  content: "";
  background-image: url("../../assets/Home/bg/cloud_top.svg");
  background-size: cover;
  background-repeat: no-repeat;
  width: 100%;
  height: 150px;
}
.bottom_cloud-bg{
  content: "";
  background-image: url("../../assets/Home/bg/cloud_bottom.svg");
  background-size: cover;
  background-repeat: no-repeat;
  width: 100%;
  height: 150px;
}
.main__content__text{
  font-size: 20px;
  line-height: 24px;
  text-align: center;
  color: #79885C;
  margin: 0 5%;
}
.main__content__text span{
  color: #7DD3CA;
  font-weight: 600;
}
@media screen and (max-width: 1334px) {
  .Our_benefits__content{
    margin: 10px 2%;
  }
}
@media screen and (max-width: 878px) {
  .test{
    justify-content: center;
    margin: 10px auto;
  }
}
@media screen and (max-width: 425px) {
  .Our_benefits__content-gif{
    max-width: 300px;
    height: 300px;
  }
  .Our_benefits__content-gif img{
    max-width: 300px;
  }
}

</style>