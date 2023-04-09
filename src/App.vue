<template>
  <div>{{ todos }}</div>
  <br />
  <form @submit.prevent="addTodo()">
    <label for="todo"
      >새로운 할 일 입력
      <hr
    /></label>
    <input type="text" id="todo" v-model="newTodo" />
    <button>추가</button>
  </form>
  <ul>
    <li v-for="todo in todos" :key="todo.id">
      <input type="checkbox" v-model="todo.done" />
      <span :class="{ done: todo.done }"> {{ todo.text }} </span>
      <button @click="removeTodo(todo)">삭제</button>
    </li>
  </ul>
</template>

<script>
let id = 0;
export default {
  name: "App",
  data() {
    return {
      newTodo: "",
      todos: [],
    };
  },
  computed: {},
  directives: {},
  methods: {
    addTodo() {
      this.todos.push({ id: id++, text: `${this.newTodo}`, done: false });
      this.newTodo = "";
    },
    removeTodo(todo) {
      this.todos = this.todos.filter((c) => {
        return c !== todo;
      });
    },
  },
  watch: {},
  components: {},
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 60px;
}
input {
  margin-right: 10px;
}
.done {
  text-decoration: line-through;
  opacity: 0.8;
}
</style>
