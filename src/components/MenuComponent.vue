<template lang="html">
  <header class="header">
    <a href="#" @click.prevent="menu = true" class="header__burger">
      <img src="@/assets/image/burger.svg" alt="меню">
    </a>
    <div class="menu" v-show="menu">
      <div class="menu__inner">
        <img src="@/assets/image/close.svg" alt="закрыть" class="menu__close" @click="menu = false">

        <div class="menu__buttons">
          <button :class="['menu__buttons_country', {'open-select': country}]" @click="country = !country">
            <span>Страны</span>
            <img src="@/assets/image/arrow.svg" alt="Страны">
            <div @click.stop="country = false" v-show="country">
              <p>Активный</p>
              <p>Майские</p>
              <p>На авто</p>
              <p>На корабле</p>
              <p>Новый год</p>
              <p>Поход</p>
              <p>Серфингp</p>
              <p>Эксклюзив</p>
              <p>Экскурсионный</p>
              <p>Экспедиция</p>
            </div>
          </button>

          <button class="menu__buttons_date">
            <span>Даты</span>
            <img src="@/assets/image/arrow.svg" alt="Даты">
          </button>
          <div class="menu__buttons_date--open">
            <date-picker v-model="time" lang="ru" range ref="datepicker"></date-picker>
          </div>
          <button :class="['menu__buttons_type', {'open-select': type}]" @click="type = !type">
            <span>Тип путешествия</span>
            <img src="@/assets/image/arrow.svg" alt="Тип путешествия">
            <div @click.stop="type = false" v-show="type">
              <p>Активный</p>
              <p>Майские</p>
              <p>На авто</p>
              <p>На корабле</p>
              <p>Новый год</p>
              <p>Поход</p>
              <p>Серфингp</p>
              <p>Эксклюзив</p>
              <p>Экскурсионный</p>
              <p>Экспедиция</p>
            </div>
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
import DatePicker from 'vue2-datepicker';
import 'vue2-datepicker/index.css';

export default {
  name: 'Menu',
  components: { DatePicker },
  data () {
    return {
      menu: true,
      time: null,
      type: false,
      country: false,
    }
  },
  methods: {
    showDate () {
      console.log(this.$refs.datepicker)
      this.$refs.datepicker.$el
    }
  }
}
</script>

<style lang="scss" scoped>
@import './../assets/scss/menu.scss';
</style>
