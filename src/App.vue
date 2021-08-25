<template>
  <HeaderApp />
  <section class="main">
    <Form />
    <TodoList v-if="todos.length > 0" @delete-product=deleteProduct :todos=todos />
    <p class="main__nocontent" v-else>Список пуст</p>
  </section>
</template>s

<script>
import { nanoid } from 'nanoid'
import HeaderApp from '@/components/HeaderApp.vue'
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
    HeaderApp,
    Form,
    TodoList
  },
  methods: {
    deleteProduct (id) {
      this.todos = this.todos.filter(product => {
        if (product.id !== id) {
          return product
        }
      })
    }
  }
}
</script>

<style lang="scss">
@import "@/styles/scss/index";
.main {
    display: grid;
    grid-template-columns: 332px 1fr;
    grid-template-rows: 1fr;
    gap: 16px;
    &__nocontent {
      font-size: 25px;
    }
}
@media all and (max-width: 1024px) {
  .main {
    grid-template-columns: 250px 1fr;
  }
}
@media all and (max-width: 900px) {
  .main {
    grid-template-columns: 200px 1fr;
}
}
</style>
