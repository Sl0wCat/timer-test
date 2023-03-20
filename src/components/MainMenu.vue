<template>
  <ul class="main-menu" id="main-menu">
    <li v-for="item in items" v-bind:key="item.text">
      <a :href="item.link">{{ item.text }}</a>
    </li>
  </ul>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  data() {
    return {
      items: [
        { link: "/", text: "Услуги" },
        { link: "/", text: "Виджеты" },
        { link: "/", text: "Интеграции" },
        { link: "/", text: "Кейсы" },
        { link: "/", text: "Сертификаты" },
      ],
    };
  },
});
</script>

<style scoped>
li {
  margin: 0 15px;
  list-style-type: none;
}
</style>
