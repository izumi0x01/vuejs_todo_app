<template>
  <div id="TodoList">
    <TodoItem />
  </div>
</template>
<script>
  import TodoItem from './components/TodoItem.vue'

  export default{
    name: 'TodoList',
    components: {
      TodoItem
    },
    data: function(){
      return{
        todos: [],
      }
    },
    methods:{
      AddTodo: function(){
        this.todos.push({content: this.todo})
        this.todo=''
      },
      RemoveTodo: function(index){
        this.todos.splice(index, 1)
      }
    }
  } 
</script>
<style>
/* #app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
