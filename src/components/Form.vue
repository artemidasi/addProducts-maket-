<template>
  <form @submit.prevent class="product__form">
    <p class="product__additional">
      Наименование товара
      <svg
        class="product__svg"
        width="4"
        height="4"
        viewBox="0 0 4 4"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <rect width="4" height="4" rx="2" fill="#FF8484" />
      </svg>
    </p>
    <input
      class="product__input"
      required
      name="name"
      type="text"
      placeholder="Введите наименование товара"
    />
    <p class="product__additional">
      Описание товара
      <svg
        class="product__svg"
        width="4"
        height="4"
        viewBox="0 0 4 4"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <rect width="4" height="4" rx="2" fill="#FF8484" />
      </svg>
    </p>
    <textarea
      class="product__textarea"
      required
      name="description"
      placeholder="Введите описание товара"
    ></textarea>
    <p class="product__additional">
      Ссылка на изображение товара
      <svg
        class="product__svg"
        width="4"
        height="4"
        viewBox="0 0 4 4"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <rect width="4" height="4" rx="2" fill="#FF8484" />
      </svg>
    </p>
    <input
      class="product__input"
      required
      type="url"
      name="link"
      placeholder="Введите ссылку"
    />
    <p class="product__additional">
      Цена товара
      <svg
        class="product__svg"
        width="4"
        height="4"
        viewBox="0 0 4 4"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <rect width="4" height="4" rx="2" fill="#FF8484" />
      </svg>
    </p>
    <input
      class="product__input"
      required
      type="number"
      name="price"
      placeholder="Введите цену"
    />
    <button class="product__button" type="submit">Добавить товар</button>
  </form>
</template>

<script>
export default {
  name: 'Form'
}
</script>

<style scoped lang="scss">
@import "../styles/scss/_variables";
@import "../styles/scss/_extension";
.product {
  &__form {
    max-height: 440px;
    padding: 24px;
    background: white;
    border-radius: 4px;
    box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.04),
      0px 6px 10px rgba(0, 0, 0, 0.02);
  }
  &__input,
  &__textarea {
    @extend %effects-element;
    @extend %form-elements;
  }
  &__input {
    &:placeholder {
      color: $color__B4;
      font-size: 12px;
      line-height: 15px;
    }
    &[name="price"] {
      margin-bottom: 24px;
    }
  }
  &__textarea {
    min-height: 108px;
  }
  &__additional {
    position: relative;
    margin-bottom: 4px;
    color: $dark;
    font-size: 10px;
    line-height: 13px;
  }
  &__svg {
    position: absolute;
  }
  &__button {
    @extend %effects-element;
    @extend %effects-button;
    padding: 10px 0;
    width: 100%;
    border-radius: 10px;
    border: 1px solid rgba(0, 0, 0, 0);
    color: $color__B4;
    background-color: $color__EE;
    font-weight: 600;
    font-size: 12px;
    line-height: 15px;
  }
}
</style>
