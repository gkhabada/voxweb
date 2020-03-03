<template>
  <div id="app">
    <menu-component />
    <tour-items :title="tour.title" :items="tour.items"/>
    <form-component />
  </div>
</template>

<script>
import MenuComponent from './components/MenuComponent.vue'
import TourItems from './components/TourItems.vue'
import FormComponent from './components/FormComponent.vue'


export default {
  name: 'App',
  components: {
    MenuComponent,
    TourItems,
    FormComponent,
  },
  data() {
    return {
      tour: {
        title: 'Зимбабве',
        items: [
          {
            title: 'Под небом Тосканы',
            place: 'ИТАЛИЯ',
            price: 'от 118 112',
            image: require('./assets/image/1.jpg'),
            way: 'Сансеполькро — (Перуджа) — Ассизи — Губбио — (Сиена) — Ла Верна — Ангиари — Монтерки — Ареццо — Кортона — (Пиенца) - (Монтепульчано)',
            details: '8 дней / 7 ночей Русский язык',
            dates: ['27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19'],
            dop_text: 'Авиаперелет включен!',
          },
          {
            title: 'Майские каникулы в Исландии',
            place: 'ИСЛАНДИЯ',
            price: '140 715',
            image: require('./assets/image/2.jpg'),
            way: 'Рейкьявик — Тингвеллир — Гюдльфосс — Скафтафедль — Сельяландсфосс — Скоугафосс — Йёкюльсаурлоун — Голубая Лагуна — Снайфельсйёкутль — Arnarstapi — Рейкьявик',
            details: '8 дней / 7 ночей Русский язык',
            dates: ['27.04.19 - 04.05.19'],
          },
          {
            title: 'Открытие Турции',
            place: 'ТУРЦИЯ',
            price: '37 302',
            image: require('./assets/image/3.jpg'),
            way: 'Стамбул — Анкара — Каппадокия — Конья — Памуккале — Эфес — Кушадасы — Пергам — Ассос — Троя — Стамбул',
            details: '8 дней / 7 ночей Русский язык',
            dates: ['27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19'],
          },
          {
            title: 'От Свальбарда до Груманта',
            place: 'НОРВЕГИЯ, ШПИЦБЕРГЕН',
            price: '145 000',
            image: require('./assets/image/1.jpg'),
            details: '8 дней / 7 ночей Русский язык',
            dates: ['27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19', '27.04.19 - 04.05.19'],
            dop_text: 'Гарантированный тур!',
          }
        ]
      }
    }
  }
}
</script>

<style lang="scss">
@import 'assets/css/normalize.css';
@import 'assets/css/font.css';

#app {
  font-family: "MuseoSansCyrl", Arial, sans-serif;
}

//date time picker

.mx-datepicker {
  width: auto!important;
}

.mx-calendar.mx-calendar-panel-date:not(:first-child) {
  display: none;
}

.mx-btn-icon-double-left, .mx-btn-icon-double-right {
  display: none;
}

</style>
