<template>
    <form @submit="onAddNewTask">
      <input type="text" v-model="NewTaskContent">
    </form>
</template>

<script>

export default {
  name: "TodoInput",
  data(){
    return{
      NewTaskContent:""
    }
  },
  methods:{
    onAddNewTask(e){
      //イベントが明示的に処理されない場合にその規定のアクションを通常通りに行うべきではないことを伝える．
      //あー，vuejsで@click.preventを定義するのと同じ理由だこれ
      e.preventDefault();

      const _NewTaskContent = this.NewTaskContent;
      this.$emit("eventAddNewTask",_NewTaskContent)
      this.NewTaskContent = ""
    }
  }
}
</script>
