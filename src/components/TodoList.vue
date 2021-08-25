<template>
  <ul class="product__list">
    <TodoItem @add-product="addProduct" :key=todo.id :todo=todo v-for="todo in todos" />
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
    addProduct (id) {
      console.log(id)
      this.$emit('add-product', id)
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
</style>
