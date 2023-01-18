<template>
  <p>You are {{ age }} years old</p>
  <button type="button" @click="updateAge">Update Age</button>
</template>

<script>
  export default{
    name: "User",
    props: {
      age: {
        type: Number,
        // required: true,
        validator(value) {
          return value < 130    
        }
      }
    },
    emits: ["update-age"],
    methods: {
      updateAge(){
          this.$emit("update-age", 3)
      }
    }
  }
</script>