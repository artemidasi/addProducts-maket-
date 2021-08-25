<template>
    <form class="product__form" action="#">
    <h2>Проверка</h2>
    <span></span>
    <input class="product__input" name="name" type="text" placeholder="Введите наименование товара">
    <textarea name="description" placeholder="Введите описание товара"></textarea>
    <input class="product__input" type="url" name="link" placeholder="Введите ссылку">
    <input class="product__input" type="number" name="price" placeholder="Введите цену">
  </form>
</template>

<script>

export default {
  name: 'Form'
}
</script>

<style scoped lang="scss">
@import '../styles/scss/_variables';
.product {
  &__form {
    padding: 24px;
    background: white;
    max-height: 440px;
  }
  &__input {
    width: 100%;
    padding: 10px 16px;
    border-radius: 4px;
    box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
    &:placeholder {
      color: $color__B4;
      font-size: 12px;
      line-height: 15px;
    }
    &:hover {
      :placeholder {
        color: $color__orange;
      }
      border: 2px solid $color__orange;
    }
  }
}
</style>
