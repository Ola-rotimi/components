<template>
  <p v-if="age > 25">Hello World!</p>
  <p v-else>You must be above 25 years old</p>
</template>

<script>
  export default{
    name: "Greeting",
    props: ["age"],
  }
</script>

<style scoped lang="scss">
p {
  color: red;

  &:hover {
    color: lighten($color: red, $amount: 15%);
  }
}
</style>
