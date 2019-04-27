<template>
  <div>
     <TodoForm v-on:submitted="saveTask"></TodoForm>
     <TodoList :todo-list="taskList"></TodoList>
  </div>
</template>

<script>
import TodoForm from "@/components/TodoForm"
import TodoList from "@/components/TodoList"
export default {
  data() {
    return {
      taskList: []
    }
  },
  components: {
    TodoForm,
    TodoList
  },
  methods: {
    saveTask(task) {
      this.taskList.push({
        text: task,
        todo: true
      });
    }
  }
}
</script>


<style lang="scss">
@import "@/assets/app.scss";

</style>
