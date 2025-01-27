<template>
  <div v-text="num" class="text-center mt-2 font-bold text-3xl underline"></div>
  <div class="bg-blue-500 text-white text-center p-3 font-serif mt-4" v-if="num === 'Hello'">Positive {{num}} {{num1}}</div>
  <div v-else>Wrong turn</div>
  <div v-show="aware">{{num1 + 123456788}}</div>
    <div v-if="aware">{{num1 + 123456788}}</div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      num: "Hello",
      num1: 1, 
      aware:true
    }
  }
}
</script>

<style>
*{
  padding: 0;
  margin: 0;
}

</style>
