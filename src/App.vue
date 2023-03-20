<template>
  <div class="balls">
    <div class="red-ball"></div>
    <div class="purple-ball"></div>
    <div class="small-ball"></div>
  </div>
  <div class="container">
    <header class="header">
      <div class="top">
        <div class="nav">
          <a href="#" class="main-link"
            ><img src="./assets/Vector.png" /><img
              src="./assets/Vector1.png"
              style="margin-left: 8px"
          /></a>
        </div>
        <div class="nav">
          <MainMenu />
        </div>

        <div class="nav contacts">
          <span class="phone">+7 555 555-55-55</span>
          <span class="links">
            <a href="/"><img src="./assets/telegram.png" /></a>
            <a href="/"><img src="./assets/phone.png" /></a>
            <a href="/"><img src="./assets/viber.png" /></a>
          </span>
        </div>
      </div>
      <div class="bot">
        <div class="slogan">
          крупный интегратор CRM в Росcии и ещё 8 странах
        </div>
      </div>
    </header>
    <div class="content">
      <div class="left">
        <h1>Зарабатывайте больше<br /><span class="orange">c WELBEX</span></h1>
        <div class="slogan">Развиваем и контролируем<br />продажи за вас</div>
      </div>
      <div class="right" id="gifts">
        <p>
          Вместе с <span class="orange">бесплатной консультацией</span> мы
          дарим:
        </p>
        <FreeGifts />
        <button class="btn-blue">Получить консультацию</button>
      </div>
    </div>
    <footer class="footer">
      <FooterMenu />

      <div class="item contacts">
        <div class="title">Контакты</div>
        <div class="phone">+7 555 555-55-55</div>
        <div class="links">
          <a href="/"><img src="./assets/telegram.png" /></a>
          <a href="/"><img src="./assets/phone.png" /></a>
          <a href="/"><img src="./assets/viber.png" /></a>
        </div>
        <div class="address">Москва, Путевой проезд 3с1, к 902</div>
      </div>
    </footer>
    <div class="copyright">
      ©WELBEX 2022. Все права защищены.<br />
      <a href="/">Политика конфиденциальности</a>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import MainMenu from "@/components/MainMenu.vue";
import FreeGifts from "@/components/FreeGifts.vue";
import FooterMenu from "@/components/FooterMenu.vue";

export default defineComponent({
  name: "App",
  components: {
    MainMenu,
    FreeGifts,
    FooterMenu,
  },
});
</script>

<style src="./style.css"></style>
