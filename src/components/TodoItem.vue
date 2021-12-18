<template>
  <div todo="TodoItem">
    <li>{{todo}}</li>
  </div>
</template>
<script>

let TodoItem = {
  props: {
    todo: String
  },
  data: function(){
    return{
      todo: ""
      }
  },
}

new Vue({
  name: "TodoItem",
  "todo-item": TodoItem
})
</script>