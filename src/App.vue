<template>
  <div>
    <h1>{{ msg}}</h1>
    <button @click="fn">翻转</button>
  </div>
</template>

<script>
export default {
 data(){
  return {
    msg: 'Hello, world!',
  }
 },
 methods:{
  fn(){
    this.msg=this.msg.split('').reverse().join('')
  }
 }
}
</script>

<style>

</style>