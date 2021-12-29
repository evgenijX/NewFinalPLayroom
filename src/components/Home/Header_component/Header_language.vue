<template>
  <v-menu offset-y>
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
          text-transform: capitalize;"
      >
        {{ language }} <img src="@/assets/Header/arrow_green.svg" alt="" style="margin-left: 10px;">
      </v-btn>
    </template>
    <v-list>
      <v-list-item @click="language = 'Укр'">
        <v-list-item-title>Укр</v-list-item-title>
      </v-list-item>
      <v-list-item @click="language = 'Рус'">
        <v-list-item-title>Рус</v-list-item-title>
      </v-list-item>
      <v-list-item @click="language = 'Eng'">
        <v-list-item-title>Eng</v-list-item-title>
      </v-list-item>
    </v-list>
  </v-menu>
</template>

<script>
export default {
  name: "Header_language",
  data: () => {
    return {
      language: 'Укр'
    };
  },
};
</script>

<style scoped>

</style>