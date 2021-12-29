<template>
  <div class="contact" style="text-align: center;">
    <div class="contact-title">Контакти</div>
    <div class="contact_content">
      <div class="contact__content-subtitle" style="
        font-size: 30px;
        color: #357364;
        font-weight: 400;
      ">Години роботи:</div>
      <div class="contact__content-text" style="
        font-size: 30px;
        color: #357364;">
        Понеділок - п'ятниця: з 8.30 до 19.00</div>
      <a href="mailto:infoplayroom18@gmail.com" style="
        text-decoration: none;
        font-size: 25px;
        color:  #BEA32E;
      ">infoplayroom18@gmail.com</a>
    </div>
    <div class="contact__buttons">
      <v-btn class="contact_btn" @click="location = 'kyiv'">Playroom Kids Club Київ</v-btn>
      <v-btn class="contact_btn" @click="location = 'kozin'">Playroom Kids Club Koзин</v-btn>
    </div>
    <Map_kyiev v-if="location === 'kyiv'" />
    <Map_Kozin v-else/>
  </div>
</template>

<script>
import Map_kyiev from "@/components/Home/Contact_component/Map_kyiev";
import Map_Kozin from "@/components/Home/Contact_component/Map_Kozin";
export default {
  name: "Contact",
  components: {Map_Kozin, Map_kyiev},
  data: () => {
    return{
      location: 'kyiv'
    }
  }
}
</script>

<style scoped>
.contact-title{
  font-weight: 800;
  font-size: 40px;
  color: #7AD4CB;
}
.contact__buttons{
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  padding: 30px 20%;

}
.contact_btn{
  margin-top: 20px;
  text-transform: capitalize;
  width: 200px;
  height: 50px !important;
  background: linear-gradient(90deg, #ECE9E6 0%, #FFFFFF 100%);
  box-shadow: 3px 3px 2px rgba(143, 176, 186, 0.8);
  border-radius: 2px;
  color: #79885C;
}
@media screen and (max-width: 375px) {

  .contact__buttons{
    padding: 30px 5%;
    justify-content: center;
  }
  .contact__content-text{
    font-size: 20px !important;
  }
  .contact_content a{
    font-size: 20px !important;
  }
  .contact_content{

  }
}

</style>