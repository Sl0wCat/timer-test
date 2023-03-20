<template>
  <div v-for="item in items" v-bind:key="item.text" class="item">
    <div v-if="windowWidth > 901">
      <p class="title">{{ item.title }}</p>
      <p>{{ item.text }}</p>
    </div>
    <div v-else class="small-gift">
      {{ item.smallText }}
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  data() {
    return {
      items: [
        {
          title: "Виджеты",
          text: "30 готовых решений",
          smallText: "Skype аудит",
        },
        {
          title: "Dashboard",
          text: "с показателями вашего бизнеса",
          smallText: "30 виджетов",
        },
        {
          title: "Skype Аудит",
          text: "отдела продаж и CRM системы",
          smallText: "Dashboard",
        },
        {
          title: "35 дней",
          text: "использования CRM",
          smallText: "Месяц аmoCRM",
        },
      ],
      title: "testTitle",
      windowWidth: window.innerWidth,
    };
  },
  mounted() {
    this.$nextTick(() => {
      window.addEventListener("resize", this.onResize);
    });
  },

  beforeUnmount() {
    window.removeEventListener("resize", this.onResize);
  },

  methods: {
    onResize() {
      this.windowWidth = window.innerWidth;
    },
  },
});
</script>

<style scoped></style>
