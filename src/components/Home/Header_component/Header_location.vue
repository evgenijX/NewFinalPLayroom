<template>
  <v-menu
    open-on-hover
    top
    offset-y>
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
        Наші садочки
        <img src="@/assets/Header/arrow_green.svg" alt="" style="margin-left: 10px;">
      </v-btn>
    </template>
    <v-list>
      <v-list-item
        v-for="(item, index) in items"
        :key="index"
      >
        <v-list-item-title>{{ item.title }}</v-list-item-title>
      </v-list-item>
    </v-list>
  </v-menu>
</template>

<script>
export default {
  name: "Header_location",
  data: () => ({
    items: [
      { title: 'Київ' },
      { title: 'Козин' },
    ],
  }),
};
</script>

<style scoped>

</style>