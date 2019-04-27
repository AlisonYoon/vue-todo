<template>
   <form v-on:submit.prevent="submittedTodo">
      <input type="text" v-model="todoText">
      <button type="submit" class="btn-primary">Submit</button>
   </form>
</template>

<script>
export default {
   data() {
      return {
         todoText: ''
      }
   },
   methods: {
      submittedTodo() {
         this.$emit("submitted", this.todoText)
         this.todoText = ''
      }
   }
}
</script>
