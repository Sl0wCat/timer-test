<template>
  <div class="item" v-for="col in cols" v-bind:key="col.title">
    <div class="title">{{ col.title }}</div>
    <div class="col" v-for="i in colsNum(col.items)" v-bind:key="i">
      <div v-for="j in 5" v-bind:key="j">
        <a
          v-if="5 * (i - 1) + j - 1 < col.items.length"
          :href="col.items[5 * (i - 1) + j - 1].link"
          >{{ col.items[5 * (i - 1) + j - 1].text }}</a
        >
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  data() {
    return {
      cols: [
        {
          title: "О компании",
          items: [
            { link: "/", text: "Партнёрская программа" },
            { link: "/", text: "Вакансии" },
          ],
        },
        {
          title: "Меню",
          items: [
            { link: "/", text: "Расчёт стоимости" },
            { link: "/", text: "Услуги" },
            { link: "/", text: "Виджеты" },
            { link: "/", text: "Интеграции" },
            { link: "/", text: "Наши клиенты" },
            { link: "/", text: "Кейсы" },
            { link: "/", text: "Благодарственные письма" },
            { link: "/", text: "Сертификаты" },
            {
              link: "https://www.youtube.com/watch?v=dQw4w9WgXcQ",
              text: "Блог на Youtube",
            },
            { link: "/", text: "Вопрос / Ответ" },
          ],
        },
      ],
    };
  },
  methods: {
    colsNum(arr: Array<object>) {
      return Math.ceil(arr.length / 5);
    },
  },
});
</script>

<style scoped></style>
