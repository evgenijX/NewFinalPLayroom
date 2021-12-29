<template>
  <div class="header_bottom">
    <div class="left_ul">
      <ul>
        <li><v-menu
          open-on-hover
          bottom
          offset-y
        >
          <template v-slot:activator="{ on, attrs }">
            <v-btn
              v-bind="attrs"
              v-on="on"
              elevation="0"
              style="
            background: none;
            color: #357364;
            font-size: 20px;
            font-weight: 500;
            text-transform: capitalize;
              "
            >
              Про нас <img src="@/assets/Header/arrow_green.svg" alt="" width="20px" style="margin-left: 5px;">
            </v-btn>
          </template>
          <v-list>
            <v-list-item
              v-for="(item, index) in about"
              :key="index"
            >
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu></li>
        <li><v-menu
          open-on-hover
          bottom
          offset-y
        >
          <template v-slot:activator="{ on, attrs }">
            <v-btn
              elevation="0"
              style="
              background: none;
              color: #357364;
              font-size: 20px;
              font-weight: 500;
              text-transform: capitalize;
              "
              v-bind="attrs"
              v-on="on"
            >
              Умови <img src="@/assets/Header/arrow_green.svg" alt="" width="20px" style="margin-left: 5px;">
            </v-btn>
          </template>
          <v-list>
            <v-list-item
              v-for="(item, index) in rules"
              :key="index"
            >
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu></li>
        <li><v-menu
          open-on-hover
          bottom
          offset-y
        >
          <template v-slot:activator="{ on, attrs }">
            <v-btn
              elevation="0"
              style="
              background: none;
              color: #357364;
              font-size: 20px;
              font-weight: 500;
              text-transform: capitalize;
              "
              v-bind="attrs"
              v-on="on"
            >
              Садок(вiк) <img src="@/assets/Header/arrow_green.svg" alt="" width="20px" style="margin-left: 5px;">
            </v-btn>
          </template>

          <v-list>
            <v-list-item
              v-for="(item, index) in age"
              :key="index"
            >
              <v-list-item-title>

                <router-link to="/group1"
                             style="color: #357364;
                             text-decoration: none;
                              " v-if="item.title === '2-3 роки'">{{ item.title }}</router-link>
                <router-link to="/"
                             style="color: #357364;
                             text-decoration: none;
                              " v-else> {{ item.title }}</router-link>
              </v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu></li>
        <li><a href="">Covid-19</a></li>
      </ul>
    </div>
    <div class="logo" style="top: 50px; position: relative"><img src="@/assets/Header/logo.svg" alt="" style="
    background-color: #fff;
    border-radius: 100%;
    border: 10px solid white;
    z-index: 2;
"></div>
    <div class="right_ul">
      <ul>
        <li><a href="#">Англійська он-лайн</a></li>
        <li><v-menu
          open-on-hover
          bottom
          offset-y
        >
          <template v-slot:activator="{ on, attrs }">
            <v-btn
              elevation="0"
              style="
              background: none;
              color: #357364;
              font-size: 20px;
              font-weight: 500;
              text-transform: capitalize;
              "
              v-bind="attrs"
              v-on="on"
            >
              Секції <img src="@/assets/Header/arrow_green.svg" alt="" width="20px" style="margin-left: 5px;">
            </v-btn>
          </template>
          <v-list>
            <v-list-item
              v-for="(item, index) in sections"
              :key="index"
            >
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu></li>
        <li><a href="#">Літній табір</a></li>
        <li><a href="">Контакти</a></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header_bottom",
  data: () => ({
    about: [
      { title: 'Наша історія' },
      { title: 'Галерея' },
      { title: 'Вчителі' },
      { title: 'Програма' },
    ],
    rules: [
      {title: 'Інфраструктура'},
      {title: 'Харчування'},
      {title: 'Розклад'},
      {title: 'Вартість'},
    ],
    age: [
      {title: '2-3 роки'},
      {title: '3-4 роки'},
      {title: '4-5 роки'},
      {title: '5-6 роки'},
      {title: '5-6 роки'},
      {title: 'DayCare'},
    ],
    sections: [
      {title: 'Айкідо'},
      {title: 'Танці'},
      {title: 'Творче мистецтво'},
    ]
  }),
}
</script>

<style scoped>
.header_bottom{
  padding: 0 5%;
  margin: 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 90px;
  border-top: 2px solid rgba(255, 209, 11, 0.5);
}
ul{
  display: flex;
  align-items: center;
}
li{
  margin-right: 20px;
  list-style: none;
}
ul a{
  color: #357364;
  font-size: 20px;
  font-weight: 500;
  text-transform: capitalize;
  text-decoration: none;
}
.v-btn:not(.v-btn--round).v-size--default{
  padding: 0 !important;
}
</style>