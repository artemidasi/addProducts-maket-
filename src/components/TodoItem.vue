<template>
  <li @click="$emit('add-product', todo.id)" class="product__item">
    <img class="product__item-photo" src='../assets/Card/card__photo.png' />
    <div class="product__item-info">
      <h3 class="product__item-title" >{{todo.title}}</h3>
      <p class="product__item-description" >{{todo.description}}</p>
      <p class="product__item-price" >{{todo.price}} рублей</p>
    </div>
  </li>
</template>

<script>
export default {
  name: 'TodoItem',
  props: {
    todo: {
      type: Object,
      required: true
    }
  },
  methods: {
    addProduct: () => {
      console.log(this)
      // this.$emit('add-product', this.todo.id)
    }
  }
}
</script>
<style scoped lang="scss">
.product {
  &__item {
    padding-bottom: 24px;
    background: white;
    border-radius: 4px;
    &-photo {
      max-width: 332px;
      margin-bottom: 16px;
    }
    &-info {
      margin: 0 16px;
    }
    &-title {
      font-size: 20px;
      line-height: 25px;
      margin-bottom: 16px;
    }
    &-description {
      margin-bottom: 32px;
      font-size: 16px;
      line-height: 20px;
    }
  }
}
</style>
