<template>
  <div>
    <li>{{Content}}</li>
  </div>
</template>

<script>

export default{
  name: "todoitem",
  props:{
    ID: {
      type: Number,
      required: true,
      default: 0
    },
    Content: {
      type: String,
      required: true,
      default: ""
    }
  }
}

</script>