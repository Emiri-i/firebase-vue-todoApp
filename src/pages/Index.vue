<template>
  <div class="mt-5">
    <h1>Todoリスト</h1>
    <todo-form @handleParentAddTodo="handleParentAddTodo" />
    <todo-list />
  </div>
</template>

<script>
import TodoForm from "@/components/TodoForm";
import TodoList from "@/components/TodoList";
export default {
  name: "Todo",
  components: {
    TodoForm,
    TodoList,
  },
  data() {
    return {
      todos: [],
    };
  },
  methods: {
    handleParentAddTodo(value) {
      if (value) {
        this.todos.push({ text: value });
      }
    },
  },
};
</script>

<style scoped></style>
