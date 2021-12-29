<template>
  <div class="timetable">
    <div class="timetable-title">Розклад дня</div>
    <div class="slider">
      <div class="select_age" style="margin-top: 20px">
        <v-menu>
          <template v-slot:activator="{ on, attrs }">
            <v-btn
              v-bind="attrs"
              v-on="on"
              elevation="0"
              style="
                background: none;
                margin-top: 10px;
                "
            >
              {{slider}} <img src="@/assets/Home/arrow_yellow.svg" alt="" style="width: 25px; margin-left: 10px;">
            </v-btn>
          </template>
          <v-list>
            <v-list-item @click="slider = 'Група дітей 2-3 роки'">
              <v-list-item-title>Група дітей 2-3 роки</v-list-item-title>
            </v-list-item>
            <v-list-item @click="slider = 'Група дітей 3-4 роки'">
              <v-list-item-title>Група дітей 3-4 роки</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>
      </div>
      <Timetable_young v-if="slider === 'Група дітей 2-3 роки'" />
      <Timetable_old v-else/>
    </div>
  </div>
</template>

<script>

import Timetable_young from "@/components/Home/Timetable_component/Timetable_young";
import Timetable_old from "@/components/Home/Timetable_component/Timetable_old";
export default {
  name: "Timetable",
  components: { Timetable_old, Timetable_young },
  data: () => {
    return {
      slider: 'Група дітей 2-3 роки'
    }
  }
}
</script>

<style scoped>
.timetable{
  display: flex;
  flex-direction: column;
  margin: 70px auto;
  align-items: center;
}
.timetable-title{
  font-weight: 800;
  font-size: 40px;
  margin-bottom: 50px;
  color: #7AD4CB;
}
.slider{
  height: 100%;
  background: #D9F6FF;
  box-shadow: 0px 3px 18px rgba(53, 115, 100, 0.3);
  border-radius: 75px;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.v-btn.v-size--default{
  font-size: 20px !important;
  color: #BEA32E;
}
</style>