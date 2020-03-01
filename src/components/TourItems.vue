<template lang="html">
  <section class="tours">
    <h1 class="tours__title">{{title || 'Название не задано'}}</h1>
    <div class="tours__items">
      <div class="tours__items_item tour__item" v-for="(tour, key) in items" :key="key">
        <div class="tour__item_head">
          <img :src="tour.image" :alt="tour.title" class="tour__item_img">
          <p class="tour__item_price">{{tour.price}} ₽</p>
        </div>
        <span class="tour__item_place">{{tour.place}}</span>
        <h3 class="tour__item_title">{{tour.title}}</h3>
        <p class="tour__item_way">{{tour.way}}</p>
        <p class="tour__item_details">{{tour.details}}</p>
        <p class="tour__item_dates">{{tour.dates[0]}} <a href="" @click.prevent=""> и показать ещё {{tour.dates.length - 1}}</a></p>
        <span class="tour__item_dop" v-if="tour.dop_text">{{tour.dop_text}}</span>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'TourItems',
  props: {
    title: String,
    items: Array
  },
}
</script>

<style lang="scss" scoped>
  @import './../assets/scss/tours.scss';
</style>
