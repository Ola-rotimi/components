<template>
  <Greeting :age="age" />
  <User :age="age" @update-age="updateAge" />
</template>

<script>
import Greeting from "@/component/Greeting.vue"
import User from "@/component/User.vue"

  export default{
    name: "App",
    components: {
      Greeting,
      User,
    },
    data() {
      return{
        age: 20,
      }
    },
    methods: {
      updateAge(num){
        this.age += num;
      }
    }
  }
</script>
