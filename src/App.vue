<template>
  <!-- <h2 class="main__title">Добавление товара</h2> -->
  <div class="main-container">
    <Form />
    <TodoList @add-product="addProduct" :todos="todos" />
  </div>
</template>s

<script>
import { nanoid } from 'nanoid'
import Form from '@/components/Form.vue'
import TodoList from '@/components/TodoList.vue'
import cardsArray from '@/data/cards.json'

const cardsArrayWithId = cardsArray.map((card) => {
  card.id = nanoid(20)
  return card
})

export default {
  name: 'App',
  data () {
    return {
      todos: cardsArrayWithId
    }
  },
  components: {
    Form,
    TodoList
  },
  methods: {
    addProduct (id) {
      this.todos = this.todos.map((product) => {
        if (product.id === id) {
          product.added = true
        }
        return product
      })
      console.log(this.todos)
    }
  }
}
</script>

<style lang="scss">
@import "@/styles/scss/index";
</style>
