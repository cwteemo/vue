<template>
  <div>
    <h2 @click="aa">首页<span>asdasdas</span></h2>
    <h2 @click="aa">首页<span>asdasdas</span></h2>
    <h2 @click="aa">首页<span>asdasdas</span></h2>
    <h2 @click="aa">首页<span>asdasdas</span></h2>
    <h2 @click="aa">首页<span>asdasdas</span></h2>

  </div>
</template>

<script>
export default {
  name: "Home",
  methods:{
    aa(){
      console.log(this.$router)
    }
  }
}
</script>

<style scoped>

</style>
