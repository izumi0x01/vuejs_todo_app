<template>
  <div>
      <TodoInput @eventAddNewTask="OnAddNewTask" />
      <ul v-for="Task in TaskList" :key="Task.ID" >
          <TodoItem :ID="Task.ID" :Content="Task.Content"/>
      </ul>
  </div>
</template>
<script>
  import TodoInput from './components/TodoInput.vue'
  import TodoItem from './components/TodoItem.vue'

  export default{
    name: "home",
    components:{
      TodoInput,
      TodoItem,
    },
    data(){
      return {
        TaskList: []
      }
    },
    methods:{
      OnAddNewTask(NewTaskContent){
          const NewTask = 
          {
            ID: this.TaskList.length,
            Content: NewTaskContent
          }
          this.TaskList.push(NewTask)
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
