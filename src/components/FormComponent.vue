<template lang="html">
  <section class="form">
    <h2 class="form__title">Заявка на подбор путеешествия </h2>

    <div class="form__item">
      <div class="form__item_title">
        <span>НЕМНОГО О ВАС</span>
      </div>
      <div class="form__field">
        <label for="name" class="form__field_label">ИМЯ <span class="form__required">*</span></label>
        <input type="text" class="form__field_input" id="name" name="name">
        <span class="form__field--error-text">Укажите имя</span>
      </div>
      <div class="form__field">
        <label for="phone" class="form__field_label">ТЕЛЕФОН</label>
        <input type="tel" id="phone" class="form__field_input" name="phone" placeholder="+7___ ___ __ __">
        <span class="form__field--error-text">Укажите имя</span>
      </div>
    </div>

    <div class="form__item">
      <div class="form__item_title">
        <span>О ПУТЕШЕСТВИИ</span>
      </div>
      <div class="form__field form__field--error">
        <label for="place" class="form__field_label">КУДА И КОГДА ХОТИТЕ ПОЕХАТЬ? <span class="form__required">*</span></label>
        <input type="text" id="place" class="form__field_input" name="place" placeholder="Континент, страна или город">
        <span class="form__field--error-text">Укажите континет, страну или город</span>
      </div>
      <div class="form__field">
        <label for="date" class="form__field_label">КОГДА?</label>
        <input type="text" id="date" class="form__field_input" name="date" placeholder="Даты или временной интервал">
        <span class="form__field--error-text">Укажите день</span>
      </div>
    </div>

    <div class="form__item checkboxs">
      <div class="form__item_title">
        <span>УДОБНЫЙ СПОСОБ СВЯЗИ</span>
      </div>
      <div class="form__checkbox">
        <input type="checkbox" class="form__checkbox_item" id="viber" name="viber">
        <label for="viber" class="form__field_label">viber<img src="@/assets/image/checked.svg" alt="checked"></label>
      </div>
      <div class="form__checkbox">
        <input type="checkbox" class="form__checkbox_item"  id="whatsapp" name="whatsapp" checked>
        <label for="whatsapp" class="form__field_label">whatsapp
        <img src="@/assets/image/checked.svg" alt="checked"></label>
      </div>
      <div class="form__checkbox">
        <input type="checkbox" class="form__checkbox_item" id="pochta" name="pochta">
        <label for="pochta" class="form__field_label">Почта<img src="@/assets/image/checked.svg" alt="checked"></label>
      </div>
      <div class="form__checkbox">
        <input type="checkbox"  class="form__checkbox_item" id="tel" name="tel">
        <label for="tel" class="form__field_label">Телефон<img src="@/assets/image/checked.svg" alt="checked"></label>
      </div>
    </div>

    <div class="form__item checkboxs">
      <div class="form__item_title">
        <span>ОТКУДА УЗНАЛИ О НАС</span>
      </div>
      <div class="form__checkbox">
        <input type="checkbox" class="form__checkbox_item" id="internet" name="internet" checked>
        <label for="internet" class="form__field_label">интернет<img src="@/assets/image/checked.svg" alt="checked"></label>
      </div>
      <div class="form__checkbox">
        <input type="checkbox" class="form__checkbox_item" id="friends" name="friends">
        <label for="friends" class="form__field_label">РЕКОМЕНДОВАЛИ ДРУЗЬЯ<img src="@/assets/image/checked.svg" alt="checked"></label>
      </div>
      <div class="form__checkbox">
          <input type="checkbox" class="form__checkbox_item" id="soc" name="soc">
        <label for="soc" class="form__field_label">СОЦ. СЕТИ<img src="@/assets/image/checked.svg" alt="checked"></label>
      </div>
      <div class="form__checkbox">
        <input type="checkbox" class="form__checkbox_item" id="go" name="go">
        <label for="go" class="form__field_label">УЖЕ ЕЗДИЛ<img src="@/assets/image/checked.svg" alt="checked"></label>
      </div>
    </div>

    <div class="form__agree">
      <input type="checkbox" id="news_agree" class="form__agree_checkbox" name="news_agree">
      <label for="news_agree" class="form__agree_label">Получать свежие предложения по электронной почте<img src="@/assets/image/checked.svg" alt="checked"></label>
      <p class="form__agree_text">Каждую неделю мы делаем для вас обзор лучших экспедиций, статей и лайфхаков для путешественников. Если вдруг вам не понравится, вы сможете отписаться в любой момент.</p>
    </div>

    <div class="form__agree">
      <input type="checkbox" id="news_agree" class="form__agree_checkbox" name="news_agree" checked>
      <label for="news_agree" class="form__agree_label">С обработкой своих персональных данных согласен. <span class="form__required">*</span><img src="@/assets/image/checked.svg" alt="checked"></label>
      <p class="form__agree_text">Отправляя заявку я подтверждаю согласие с условиями Пользовательского соглашения</p>
    </div>

    <p class="form__required_text"><span class="form__required">*</span> Поля, которые надо обязательно заполнить</p>

    <button type="button" name="button" class="form__button">
      <span>ОТПРАВИТЬ</span>
      <img src="@/assets/image/arrow.svg" alt="ОТПРАВИТЬ">
    </button>

  </section>
</template>

<script>
export default {
}
</script>

<style lang="scss" scoped>
  @import './../assets/scss/form.scss';
</style>
