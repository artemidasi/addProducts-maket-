<template>
  <ul class="product__list">
    <TodoItem @delete-product=deleteProduct :key=todo.id :todo=todo v-for="todo in todos" />
  </ul>
</template>

<script>
import TodoItem from '@/components/TodoItem.vue'
export default {
  name: 'TodoList',
  props: ['todos'],
  components: {
    TodoItem
  },
  methods: {
    deleteProduct (id) {
      this.$emit('delete-product', id)
    }
  }
}
</script>

<style scoped lang="scss">
.product__list {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(2, 1fr);
  gap: 16px;
}
@media all and (max-width: 900px) {
  .product__list {
    grid-template-columns: repeat(2, 1fr);
    }
}
</style>
