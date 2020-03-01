<template lang="html">
  <header class="header">
    <a href="#" @click.prevent="menu = true" class="header__burger">
      <img src="@/assets/image/burger.svg" alt="меню">
    </a>
    <div class="menu" v-show="menu">
      <div class="menu__inner">
        <img src="@/assets/image/close.svg" alt="закрыть" class="menu__close" @click="menu = false">

        <div class="menu__buttons">
          <button class="menu__buttons_country">
            <span>Страны</span>
            <img src="@/assets/image/arrow.svg" alt="Страны">
          </button>
          <button class="menu__buttons_date">
            <span>Даты</span>
            <img src="@/assets/image/arrow.svg" alt="Даты">
          </button>
          <button class="menu__buttons_type">
            <span>Тип путешествия</span>
            <img src="@/assets/image/arrow.svg" alt="Тип путешествия">
          </button>
          <a href="#" class="menu__button--outline">
            НАЙТИ
          </a>
        </div>

        <ul class="menu__links">
          <li><a href="" class="menu__link">ПУТЕШЕСТВИЯ</a></li>
          <li><a href="" class="menu__link">О НАС</a></li>
          <li><a href="" class="menu__link">ОТЗЫВЫ</a></li>
          <li><a href="" class="menu__link">БЛОГ</a></li>
        </ul>

        <a href="tel:+74951234567" class="menu__phone">+7 (495) 123-45-67</a>
        <a href="" class="menu__button--outline">ПОДБЕРИТЕ МНЕ ТУР</a>

      </div>
    </div>
  </header>
</template>

<script>

export default {
  name: 'Menu',
  data () {
    return {
      menu: false,
    }
  }
}
</script>

<style lang="scss" scoped>
@import './../assets/scss/menu.scss';
</style>
