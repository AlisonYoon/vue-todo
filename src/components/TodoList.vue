<template>
   <div>
      <ul>
         <li 
            v-for="(item, index) in todoItems" 
            :key="index"
         >
            {{ item.text }}
         </li>
      </ul>
   </div>
</template>

<script>

export default {
   props: {
      todoList: {
         type : Array,
         required : true
      }
   },
   computed: {
      todoItems() {
         return this.todoList.filter(i => i.todo)
      }
   }
}
</script>
