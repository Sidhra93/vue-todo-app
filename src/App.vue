<template>
  <div id="app">
    <todo-list :todos="todos"></todo-list>
    <create-todo @add-todo="addTodo"></create-todo>
  </div>
</template>

<script>
import TodoList from './components/TodoList'
import CreateTodo from './components/CreateTodo'

export default {
  name: 'App',
  components: {
    TodoList,
    CreateTodo
  },
  data () {
    return {
      todos: [{
        title: 'Todo A',
        project: 'Project A',
        done: false
      }, {
        title: 'Todo B',
        project: 'Project B',
        done: true
      }, {
        title: 'Todo C',
        project: 'Project C',
        done: false
      }, {
        title: 'Todo D',
        project: 'Project D',
        done: false
      }]
    }
  },
  methods: {
    addTodo (todo) {
      this.todos.push({
        title: todo.title,
        project: todo.project,
        done: false
      })
      // console.log(to do)
    }
  }
}
</script>
